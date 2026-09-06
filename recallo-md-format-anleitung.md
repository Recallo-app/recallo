# Anleitung: Recallo-Lerninhalte im .md-Format erstellen

> **Für LLMs:** Dieses Dokument beschreibt das vollständige Importformat der Lern-App "Recallo". Wenn du gebeten wirst, eine `.md`-Datei mit Lerninhalten für Recallo zu erstellen, halte dich exakt an die hier beschriebene Syntax — auch kleine Abweichungen (falsche Einrückung, fehlende Leerzeilen, falsche Groß-/Kleinschreibung bei Schlüsselwörtern) führen dazu, dass der Import fehlschlägt oder Inhalte falsch zugeordnet werden.

## 1. Grundprinzip

Eine `.md`-Datei entspricht **einem Fach** (einem Lernpfad). Sie besteht aus bis zu vier Blöcken, die als H1-Überschriften (`#`) beginnen:

```markdown
# Fach: <Name des Fachs>

# Test
... Kapitel mit Aufgaben (Klausur-/Übungsteil) ...

# Karten
... Karteikarten zum Wiederholen ...

# Nachschlag
... Referenz-Einträge (Nachschlagewerk) ...
```

Regeln:
- `# Fach: <Name>` **muss** die erste nicht-leere Zeile der Datei sein.
- `# Test`, `# Karten`, `# Nachschlag` sind optional, aber jeweils **höchstens einmal** erlaubt. Reihenfolge ist beliebig.
- Eine Datei ohne `# Test` und ohne `# Karten` ist zwar technisch gültig, aber inhaltsleer — in der Praxis sollte mindestens einer der beiden Blöcke gefüllt sein.

---

## 2. Block `# Test` — Kapitel und Aufgaben

```markdown
# Test
## <Kapiteltitel>
<Ein-Zeilen-Untertitel des Kapitels>

### Aufgabe
Typ: <radio|checkbox|truefalse|fillblank|block>
Titel: <optional, sonst automatisch "Übung X.Y">
F: <Frage>
A: <Erklärung, wird nach dem Lösen angezeigt>
H1: <optionaler Hinweis 1>
H2: <optionaler Hinweis 2>
...bis H5...
<typ-spezifische Felder, siehe unten>

### Aufgabe
...
```

- `##` = ein Kapitel. Die **erste Zeile direkt danach**, die kein Feldpräfix ist, wird automatisch der Kapitel-Untertitel.
- `###` = eine Aufgabe. Muss innerhalb eines `##`-Kapitels stehen.
- `F:` und `A:` können mehrzeilig sein — der Text läuft bis zur nächsten Feldzeile oder Überschrift weiter.
- `H1:` bis `H5:` sind optional, maximal 5, werden in der App nacheinander aufdeckbar angezeigt.
- Inline-Markdown ist erlaubt: `**fett**` und `` `code` ``.

### 2.1 Typ `radio` — eine richtige Antwort

```markdown
### Aufgabe
Typ: radio
F: Welcher Schlüsseltyp verweist auf eine andere Tabelle?
O: Primärschlüssel
O: *Fremdschlüssel
O: Superschlüssel
A: Fremdschlüssel realisieren Beziehungen zwischen Tabellen.
```
`O:` = eine Option pro Zeile. Genau **eine** Zeile trägt ein `*` direkt vor dem Text — das ist die korrekte Antwort.

### 2.2 Typ `checkbox` — eine oder mehrere richtige Antworten

```markdown
### Aufgabe
Typ: checkbox
F: Welche der folgenden sind SQL-Typen?
O: *INTEGER
O: *TEXT
O: Kilogramm
O: Meter
A: INTEGER und TEXT sind Standard-SQL-Datentypen.
```
Wie `radio`, aber **mindestens eine** Option trägt `*`; mehrere sind erlaubt.

### 2.3 Typ `truefalse` — Wahr/Falsch

```markdown
### Aufgabe
Typ: truefalse
F: Ein Primärschlüssel darf NULL-Werte enthalten.
L: false
A: Primärschlüssel sind implizit NOT NULL und UNIQUE.
```
`L:` ist **genau eine** Zeile mit dem Wert `true` oder `false` (englisch, klein geschrieben).

### 2.4 Typ `fillblank` — Lücken im Fließtext

Lücken stehen direkt im `F:`-Text in doppelten geschweiften Klammern `{{ }}`. Zwei Lückenarten, auch gemischt in einer Aufgabe:

- **Freitext-Lücke:** `{{Lösung}}` — mehrere akzeptierte Schreibweisen mit `;` trennen: `{{Zielvariable;Label;Target}}`
- **Auswahl-Lücke (Dropdown):** Optionen mit `|` trennen, korrekte mit `*` markieren: `{{Hoth|*Dagobah|Endor}}`

```markdown
### Aufgabe
Typ: fillblank
F: Der Imperator regiert das {{Galaktische Republik|*Galaktische Imperium|Jedi-Orden}}. Der Millennium Falke wird von {{Han Solo;Han}} geflogen.
A: Nach dem Sturz der Republik errichtet Palpatine das Galaktische Imperium.
```
- Text außerhalb von `{{ }}` ist normaler Fließtext.
- Literale geschweifte Klammern (kein Lückenfeld) in Code-Spans (`` `{{...}}` ``) setzen — die werden nicht als Lücke erkannt.
- Mindestens eine Lücke ist Pflicht; jede Auswahl-Lücke braucht genau ein `*`.

### 2.5 Typ `block` — Karten Spalten zuordnen (Drag & Drop)

```markdown
### Aufgabe
Typ: block
F: Ordne jeden Film seiner Episodennummer zu.
S: Episode IV
S: Episode V
S: Episode VI
K: Eine neue Hoffnung -> Episode IV
K: Das Imperium schlägt zurück -> Episode V
K: Die Rückkehr der Jedi-Ritter -> Episode VI
A: Die Original-Trilogie umfasst die Episoden IV, V und VI.
```
- `S:` = eine Zielspalte pro Zeile (2–5 Spalten sinnvoll).
- `K: <Kartentext> -> <Zielspalte>` — die Zielspalte muss **exakt** einer `S:`-Zeile entsprechen (Text muss übereinstimmen).
- Mehrere Karten dürfen auf dieselbe Spalte zeigen; jede Karte hat genau eine Zielspalte.

---

## 3. Block `# Karten` — Karteikarten (flach, keine Kapitel-Gruppierung)

```markdown
# Karten
## Karte 1
<Tag 1> | <Tag 2> | <Tag 3>
F: <Frage>
A: <Antwort>

## Karte 2
<Tags>
F: ...
A: ...
```

- Jede `##`-Überschrift ist **eine Karte**. Der Überschriftentext selbst ("Karte 1", "Karte 2" ...) ist frei wählbar und wird nicht ausgewertet — nur die Reihenfolge zählt.
- Die **erste Zeile direkt danach** ist die Tag-Zeile: beliebig viele Tags, getrennt durch `|`. Tags haben **keine feste Bedeutung** (kein "erster Tag = Kapitel" o. ä.) — es sind freie Schlagworte, nach denen später in der App gefiltert/gruppiert wird.
- **Wichtig:** Entspricht ein Tag exakt (ohne Berücksichtigung von Groß-/Kleinschreibung und Leerzeichen) einem Kapiteltitel aus dem `# Test`-Block, erzeugt das automatisch einen "Thema vertiefen"-Link zu diesem Kapitel. Das ist optional — Karten ohne passenden Tag funktionieren genauso, zeigen nur keinen Link.
- `F:` und `A:` wie bei Aufgaben, auch mehrzeilig möglich.

---

## 4. Block `# Nachschlag` — Referenz-/Nachschlagewerk

```markdown
# Nachschlag
## <Titel des Eintrags>
<Ein-Zeilen-Untertitel>
<Beliebiger Markdown-Inhalt: Aufzählungen, **Fettdruck**, `Inline-Code`, Codeblöcke>

## <Nächster Eintrag>
...
```

- `##` = ein Eintrag. Erste Zeile danach = Untertitel, alles Weitere bis zur nächsten `##` = Inhalt.
- Der Inhalt wird als vollwertiges Markdown gerendert (Aufzählungszeichen `-`, Nummerierung, ` ```codeblock``` `, `**fett**`, `` `inline code` ``).
- Diese Einträge sind reine Referenz ohne Fortschrittstracking — im Gegensatz zu Aufgaben/Karten gibt es hier kein Richtig/Falsch.

---

## 5. Allgemeine Regeln (für alle Blöcke)

- **Encoding:** UTF-8 (mit oder ohne BOM), Zeilenumbrüche LF oder CRLF — beides wird akzeptiert.
- **Feldpräfixe** (`F:`, `A:`, `H1:`–`H5:`, `Typ:`, `Titel:`, `O:`, `L:`, `S:`, `K:`) stehen immer am Zeilenanfang.
- **Mehrzeilige Werte:** `F:` und `A:` laufen weiter, bis die nächste Feldzeile oder eine neue Überschrift (`##`/`###`) kommt — dazwischenliegende Leerzeilen werden ignoriert, der Text wird zusammengefügt.
- Ein `Titel:`-Feld bei einer Aufgabe überschreibt die automatische Beschriftung ("Übung X.Y") — meist nicht nötig, nur bei Bedarf setzen.

### Typische Fehler, die den Import abbrechen lassen
- `# Fach:` fehlt oder ist nicht die erste Zeile
- `###` (Aufgabe) außerhalb eines `##`-Kapitels
- `radio`/`truefalse` ohne genau eine korrekte Antwort markiert
- `checkbox` ohne jede markierte Antwort
- `fillblank` ohne mindestens eine `{{ }}`-Lücke, oder eine Auswahl-Lücke ohne genau ein `*`
- `block` mit einer `K:`-Zeile, deren Zielspalte nicht als `S:` existiert
- Eine Karte ohne `F:` oder ohne `A:`

Diese Fehler zeigen beim Import Zeilennummer + Klartextmeldung — bitte beim Erzeugen einer Datei diese Fälle von vornherein vermeiden.

---

## 6. Vollständiges Beispiel-Template

Kopiere diese Struktur und ersetze die Inhalte — sie deckt alle Aufgabentypen und beide Blöcke exemplarisch ab:

```markdown
# Fach: <Fachname>

# Test
## <Kapitel 1 Titel>
<Kapitel-1-Untertitel>

### Aufgabe
Typ: radio
F: <Frage mit einer richtigen Antwort>
O: <falsche Option>
O: *<richtige Option>
O: <falsche Option>
A: <Erklärung>

### Aufgabe
Typ: checkbox
F: <Frage mit mehreren richtigen Antworten>
O: *<richtige Option 1>
O: *<richtige Option 2>
O: <falsche Option>
A: <Erklärung>

### Aufgabe
Typ: truefalse
F: <Aussage>
L: true
A: <Erklärung>

### Aufgabe
Typ: fillblank
F: <Satz mit {{Lücke;Alternative}} und einer Auswahl {{Option A|*Option B|Option C}}>
A: <Erklärung>

## <Kapitel 2 Titel>
<Kapitel-2-Untertitel>

### Aufgabe
Typ: block
F: <Zuordnungsaufgabe>
S: <Spalte 1>
S: <Spalte 2>
K: <Karte 1> -> <Spalte 1>
K: <Karte 2> -> <Spalte 2>
A: <Erklärung>

# Karten
## Karte 1
<Kapitel 1 Titel> | Selbst bewerten
F: <Frage>
A: <Antwort>

## Karte 2
<freies Schlagwort>
F: <Frage>
A: <Antwort>

# Nachschlag
## <Referenz-Titel>
<Untertitel>
- <Stichpunkt>
- <Stichpunkt mit **wichtigem Begriff**>

`<Codebeispiel falls passend>`
```

---

## 7. Große Mengen erzeugen (mehrere Kapitel, viele Aufgaben pro Kapitel)

Bei Aufträgen wie "6 Kapitel mit je 25 Aufgaben zu Thema X" zusätzlich beachten:

- **Aufgabentypen mischen, nicht nur `radio` verwenden.** Als Richtwert pro Kapitel: überwiegend `radio`/`checkbox`/`truefalse` (leicht zu erstellen, decken Faktenwissen ab), dazu einige `fillblank` (für Begriffe/Definitionen) und 1–3 `block`-Aufgaben (für Zuordnungswissen, z. B. Kategorien, Reihenfolgen, Ursache-Wirkung). Nicht alle 25 Aufgaben eines Kapitels vom selben Typ.
- **Schwierigkeit innerhalb eines Kapitels steigern** — die ersten Aufgaben eines Kapitels einfacher/grundlegender, gegen Ende anspruchsvoller/verknüpfender.
- **Keine Wiederholung von Fragen** über Kapitel hinweg, auch nicht in leicht umformulierter Form — bei 150 Aufgaben (6×25) ist das die häufigste Schwachstelle.
- **Kapitel-Untertitel** kurz und beschreibend halten (ein Satz, kein Aufzählungsstil).
- **Hints (`H1`–`H5`) nicht bei jeder Aufgabe** — nur bei Aufgaben, die erfahrungsgemäß schwerfallen, sonst wird die Datei unnötig lang.
- Ob zusätzlich ein `# Karten`- und/oder `# Nachschlag`-Block gewünscht ist, **im Auftrag explizit dazusagen** — sonst fokussiert sich das LLM meist nur auf `# Test`, da das der Hauptteil des Auftrags war.

**Beispiel-Prompt für den Einsatz:**

> Lies die angehängte Anleitung (Recallo-.md-Format). Erstelle mir eine Recallo-Importdatei zum Thema "<Thema>" mit 6 Kapiteln und je 25 Aufgaben pro Kapitel. Mische die Aufgabentypen sinnvoll (überwiegend radio/checkbox/truefalse, einige fillblank, 1–3 block pro Kapitel), steigere die Schwierigkeit innerhalb jedes Kapitels, und vermeide inhaltliche Wiederholungen zwischen den Kapiteln. Ergänze zusätzlich einen `# Karten`-Block mit rund 20 Karteikarten zu den wichtigsten Begriffen, mit Tags passend zu den Kapiteltiteln.

---

## 8. Checkliste vor der Ausgabe (für das LLM)

Bevor du eine fertige `.md`-Datei ausgibst, prüfe:

- [ ] `# Fach:` ist die erste nicht-leere Zeile
- [ ] Jede `###`-Aufgabe hat `Typ:`, `F:`, und mindestens eine gültige Antwortmarkierung für ihren Typ
- [ ] Jede `radio`/`truefalse`-Aufgabe hat **genau eine** korrekte Antwort
- [ ] Jede `checkbox`-Aufgabe hat **mindestens eine** korrekte Antwort
- [ ] Jede `fillblank`-Aufgabe hat **mindestens eine** `{{ }}`-Lücke, jede Auswahl-Lücke genau ein `*`
- [ ] Jede `block`-Aufgabe: jede `K:`-Zeile zeigt auf eine tatsächlich vorhandene `S:`-Spalte
- [ ] Jede Karte hat `F:` und `A:`
- [ ] Keine doppelten `# Test`/`# Karten`/`# Nachschlag`-Blöcke
