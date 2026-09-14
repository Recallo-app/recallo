# Guide: Creating Recallo Learning Content in .md Format

> **For LLMs:** This document describes the complete import format for the "Recallo" learning app. If you are asked to create a `.md` file with learning content for Recallo, follow the syntax described here exactly — even small deviations (wrong indentation, missing blank lines, wrong capitalization of keywords) will cause the import to fail or content to be assigned incorrectly.

> ⚠️ **CRITICAL — read this before writing anything:** This guide is written in English, but the **structural keywords themselves are NOT English words to translate — they are fixed, hardcoded tokens the parser searches for literally.** They originate from German (the app's original language) and must be reproduced **exactly as shown below, verbatim, regardless of the language of your actual content.** Do **not** translate `# Fach:` to `# Subject:`, do **not** turn `F:` into `Q:`, do **not** turn `A:` into `Answer:`, do **not** rename `# Test`/`# Karten`/`# Nachschlag`. Doing so will break the import silently or with a parse error. Only the human-readable *content* inside these fields (questions, answers, chapter titles, card text, wiki content) should be in English.

> **Note on terminology:** The app's user interface currently shows **"Track"** instead of "Fach" and **"Wiki"** instead of "Nachschlag" — these are display labels only. The format keywords in the `.md` file (`# Fach:`, `# Nachschlag`) are independent of this and remain **exactly as written**, no matter what the app calls them in the UI.

## 1. Basic Principle

A `.md` file corresponds to **one Track** (called "Fach" at the file-format level). It consists of up to four blocks, each starting with an H1 heading (`#`):

```markdown
# Fach: <Track name>

# Test
... chapters with tasks (exam/practice section) ...

# Karten
... flashcards for spaced repetition ...

# Nachschlag
... reference entries (wiki) ...
```

Rules:
- `# Fach: <Name>` **must** be the first non-blank line of the file.
- `# Test`, `# Karten`, `# Nachschlag` are optional, but each allowed **at most once**. Order doesn't matter.
- A file with neither `# Test` nor `# Karten` is technically valid but empty of content — in practice, at least one of the two blocks should be filled.

---

## 2. Block `# Test` — Chapters and Tasks

```markdown
# Test
## <Chapter title>
<One-line chapter subtitle>

### Aufgabe
Typ: <radio|checkbox|truefalse|fillblank|block>
Titel: <optional, otherwise auto-generated as "Übung X.Y">
F: <Question>
A: <Explanation, shown after solving>
H1: <optional hint 1>
H2: <optional hint 2>
...up to H5...
<type-specific fields, see below>

### Aufgabe
...
```

- `##` = one chapter. The **first line right after it** that is not a field prefix automatically becomes the chapter subtitle.
- `###` = one task. Must be inside a `##` chapter. **Keep the literal word "Aufgabe" after `###`** — it is the fixed heading marker, not a label to translate to "Task" or "Question".
- `F:` and `A:` can span multiple lines — the text continues until the next field line or heading.
- `H1:` through `H5:` are optional, maximum 5, revealed one at a time in the app.
- **If `Typ:` is omitted entirely, the parser silently defaults to `radio`** — this does not cause an error but can produce an unintentionally wrong task type. Always set `Typ:` explicitly, even for radio tasks.
- Inline markdown is allowed: `**bold**` and `` `code` ``.

### 2.1 Type `radio` — one correct answer

```markdown
### Aufgabe
Typ: radio
F: Which key type references another table?
O: Primary key
O: *Foreign key
O: Super key
A: Foreign keys implement relationships between tables.
```
`O:` = one option per line. **Exactly one** line carries a `*` directly before the text — that's the correct answer. **Zero or more than one** marked option aborts the import with an error.

### 2.2 Type `checkbox` — one or more correct answers

```markdown
### Aufgabe
Typ: checkbox
F: Which of the following are SQL data types?
O: *INTEGER
O: *TEXT
O: Kilogram
O: Meter
A: INTEGER and TEXT are standard SQL data types.
```
Same as `radio`, but **at least one** option carries `*`; multiple are allowed and common.

### 2.3 Type `truefalse` — True/False

```markdown
### Aufgabe
Typ: truefalse
F: A primary key may contain NULL values.
L: false
A: Primary keys are implicitly NOT NULL and UNIQUE.
```
`L:` is **exactly one** line with the value `true` or `false` (English, lowercase — this is fixed syntax, not translatable) — any other value aborts the import.

### 2.4 Type `fillblank` — Blanks in running text

Blanks appear directly in the `F:` text as double curly braces `{{ }}`. Two kinds of blanks, which can also be mixed in one task:

- **Free-text blank:** `{{Answer}}` — separate multiple accepted spellings with `;`: `{{Target variable;Label;Target}}`. Matching against the user's input is **tolerant**: case-insensitive, leading/trailing whitespace trimmed, repeated spaces collapsed. You do **not** need to list case or spacing variants separately.
- **Choice blank (dropdown):** separate options with `|`, mark the correct one with `*`: `{{Hoth|*Dagobah|Endor}}`. Exactly **one** `*` per choice blank is required.

```markdown
### Aufgabe
Typ: fillblank
F: The Emperor rules the {{Galactic Republic|*Galactic Empire|Jedi Order}}. The Millennium Falcon is flown by {{Han Solo;Han}}.
A: After the fall of the Republic, Palpatine establishes the Galactic Empire.
```
- Text outside `{{ }}` is plain running text.
- Put literal curly braces (not meant as a blank) inside code spans (`` `{{...}}` ``) — those are not treated as blanks.
- At least one blank is required; every choice blank needs exactly one `*`.

### 2.5 Type `block` — Match cards to columns (drag & drop)

```markdown
### Aufgabe
Typ: block
F: Match each film to its episode number.
S: Episode IV
S: Episode V
S: Episode VI
K: A New Hope -> Episode IV
K: The Empire Strikes Back -> Episode V
K: Return of the Jedi -> Episode VI
A: The Original Trilogy comprises Episodes IV, V, and VI.
```
- `S:` = one target column per line (2–5 columns is reasonable).
- `K: <card text> -> <target column>` — the target column must **exactly** match one `S:` line (text must match; it is trimmed, so spacing right around `->` doesn't matter).
- Multiple cards may point to the same column; each card has exactly one target column.

---

## 3. Block `# Karten` — Flashcards (flat, no chapter grouping)

```markdown
# Karten
## Karte 1
<Tag 1> | <Tag 2> | <Tag 3>
F: <Question>
A: <Answer>

## Karte 2
<Tags>
F: ...
A: ...
```

- Each `##` heading is **one card**. The heading text itself ("Karte 1", "Karte 2", ...) is freely chosen and not evaluated by the parser — only the order matters. **Keep the literal word "Karte" after `##`** for consistency with the format spec, even though the parser itself doesn't check this specific text.
- The **first line right after it** is the tag line: any number of tags, separated by `|`. Tags have **no fixed meaning** (no "first tag = chapter" rule or similar) — they are free keywords used later for filtering/grouping in the app.
- **Important:** If a tag exactly matches (case-insensitive, whitespace-trimmed) a chapter title from the `# Test` block, this automatically creates a "Dive deeper" link to that chapter. This is optional — cards without a matching tag work exactly the same, they just don't show a link.
- `F:` and `A:` work as with tasks, multi-line is fine too.

---

## 4. Block `# Nachschlag` — Reference/Wiki Entries

```markdown
# Nachschlag
## <Entry title>
<One-line subtitle>
<Any markdown content: bullet lists, **bold text**, `inline code`, code blocks>

## <Next entry>
...
```

- `##` = one entry. First line after it = subtitle, everything else until the next `##` = content.
- The content is rendered as full markdown (bullet points `-`, numbered lists, ` ```code blocks``` `, `**bold**`, `` `inline code` ``).
- These entries are pure reference material with no progress tracking — unlike tasks/cards, there is no right/wrong here.
- The app's UI calls this section "Wiki" — the format keyword remains `# Nachschlag` regardless.

---

## 5. General Rules (for all blocks)

- **Encoding:** UTF-8 (with or without BOM), line endings LF or CRLF — both are accepted.
- **Field prefixes** (`F:`, `A:`, `H1:`–`H5:`, `Typ:`, `Titel:`, `O:`, `L:`, `S:`, `K:`) always appear at the start of a line and stay **exactly in this form** — even in files whose content is written in a different language (see Section 9).
- **Multi-line values:** `F:` and `A:` continue until the next field line or a new heading (`##`/`###`) — blank lines in between are ignored, the text is joined together.
- A `Titel:` field on a task overrides the auto-generated label ("Übung X.Y") — usually not needed, only set it when required.
- For `radio`/`checkbox` options, a `*` **directly before the option text** marks the correct answer. If an option's text itself needs to start with an asterisk, this currently can't be cleanly distinguished — in practice this rarely comes up, but when in doubt, rephrase the option so it doesn't start with `*`.

### Typical errors that abort the import
- `# Fach:` is missing or is not the first line
- `###` (a task) appears outside a `##` chapter
- `radio`/`truefalse` without **exactly one** correct answer marked (neither zero nor more than one)
- `checkbox` without any marked answer
- `fillblank` without at least one `{{ }}` blank, or a choice blank without exactly one `*`
- `block` with a `K:` line whose target column doesn't exist as an `S:` line
- A card missing `F:` or `A:`

These errors are shown on import with a line number and plain-text message — please avoid these cases when generating a file.

---

## 6. Complete Example Template

Copy this structure and replace the content — it covers all task types and both blocks by example:

```markdown
# Fach: <Track name>

# Test
## <Chapter 1 title>
<Chapter 1 subtitle>

### Aufgabe
Typ: radio
F: <Question with one correct answer>
O: <wrong option>
O: *<correct option>
O: <wrong option>
A: <Explanation>

### Aufgabe
Typ: checkbox
F: <Question with multiple correct answers>
O: *<correct option 1>
O: *<correct option 2>
O: <wrong option>
A: <Explanation>

### Aufgabe
Typ: truefalse
F: <Statement>
L: true
A: <Explanation>

### Aufgabe
Typ: fillblank
F: <Sentence with {{blank;alternative}} and a choice {{Option A|*Option B|Option C}}>
A: <Explanation>

## <Chapter 2 title>
<Chapter 2 subtitle>

### Aufgabe
Typ: block
F: <Matching task>
S: <Column 1>
S: <Column 2>
K: <Card 1> -> <Column 1>
K: <Card 2> -> <Column 2>
A: <Explanation>

# Karten
## Karte 1
<Chapter 1 title> | Self-assessed
F: <Question>
A: <Answer>

## Karte 2
<free keyword>
F: <Question>
A: <Answer>

# Nachschlag
## <Reference title>
<Subtitle>
- <Bullet point>
- <Bullet point with **important term**>

`<Code example if relevant>`
```

---

## 7. Generating Large Volumes (multiple chapters, many tasks per chapter)

For requests like "6 chapters with 25 tasks each on topic X," also keep in mind:

- **Mix task types — don't just use `radio`.** As a rule of thumb per chapter: mostly `radio`/`checkbox`/`truefalse` (easy to create, cover factual knowledge), plus some `fillblank` (for terms/definitions) and 1–3 `block` tasks (for matching knowledge, e.g., categories, sequences, cause-and-effect). Not all 25 tasks in a chapter should be the same type.
- **Increase difficulty within a chapter** — the first tasks of a chapter simpler/more basic, later ones more advanced/interconnected.
- **No repeated questions** across chapters, not even in slightly reworded form — with 150 tasks (6×25), this is the most common weakness.
- Keep **chapter subtitles** short and descriptive (one sentence, not a bullet list).
- **Don't add hints (`H1`–`H5`) to every task** — only to tasks that are typically difficult, otherwise the file becomes unnecessarily long.
- Whether a `# Karten` and/or `# Nachschlag` block is also wanted should be **stated explicitly in the request** — otherwise the LLM will usually focus only on `# Test`, since that was the main part of the request.

**Example prompt for this use case:**

> Read the attached guide (Recallo .md format). Create a Recallo import file on the topic "<Topic>" with 6 chapters and 25 tasks per chapter. Mix task types sensibly (mostly radio/checkbox/truefalse, some fillblank, 1–3 block per chapter), increase difficulty within each chapter, and avoid content repetition across chapters. Also add a `# Karten` block with about 20 flashcards on the key terms, with tags matching the chapter titles.

---

## 8. Checklist Before Output (for the LLM)

Before outputting a finished `.md` file, check:

- [ ] `# Fach:` is the first non-blank line
- [ ] Every `###` Aufgabe has `Typ:` **explicitly set** (not omitted), `F:`, and at least one valid answer marker for its type
- [ ] Every `radio`/`truefalse` task has **exactly one** correct answer (not zero, not multiple)
- [ ] Every `checkbox` task has **at least one** correct answer
- [ ] Every `fillblank` task has **at least one** `{{ }}` blank, every choice blank exactly one `*`
- [ ] Every `block` task: every `K:` line points to an `S:` column that actually exists
- [ ] Every card has `F:` and `A:`
- [ ] No duplicate `# Test`/`# Karten`/`# Nachschlag` blocks
- [ ] **None of the structural keywords have been translated** (`# Fach:`, `# Test`, `# Karten`, `# Nachschlag`, `### Aufgabe`, `Typ:`, `Titel:`, `F:`, `A:`, `O:`, `L:`, `S:`, `K:`, `H1:`–`H5:`, and the type values `radio`/`checkbox`/`truefalse`/`fillblank`/`block`)

---

## 9. Why German Keywords in an English Guide?

This may look unusual: an English-language guide instructing you to keep German-named tokens like `Fach`, `Typ`, and `Karten`. The reason is simple — Recallo's parser is hardcoded to look for these **exact strings**; they are not display text, they are the file format's syntax, comparable to keywords in a programming language (you wouldn't translate `if`/`else` into another language either). Whatever language your actual learning content is in, the skeleton stays identical:

`# Fach:`, `# Test`, `# Karten`, `# Nachschlag`, `### Aufgabe`, `Typ:`, `Titel:`, `F:`, `A:`, `O:`, `L:`, `S:`, `K:`, `H1:`–`H5:`, plus the type values `radio`, `checkbox`, `truefalse`, `fillblank`, `block`, and the values `true`/`false` for `L:`.

An English-content file looks like this:

```markdown
# Fach: World War II

# Test
## Key Events
Major turning points of the war

### Aufgabe
Typ: radio
F: In which year did World War II begin?
O: 1938
O: *1939
O: 1940
O: 1941
A: Germany invaded Poland on September 1, 1939.
```

Only `World War II`, `Key Events`, `Major turning points...`, the question, and the options are in English — `# Fach:`, `# Test`, `### Aufgabe`, `Typ:`, `radio`, `F:`, `O:`, `A:` remain exactly as shown here.
