# Fach: Softwaretechnik

# Test
## Prinzipien und Modellbegriff
Grundsätze richtigen Handelns, der Systembegriff und die drei Dimensionen der Basiskonzepte.

### Aufgabe
Typ: radio
F: Welches Prinzip bildet nach Balzert die Wurzel des Abhängigkeitsgraphen, auf der alle anderen aufbauen?
O: Verbalisierung
O: *Abstraktion
O: Modularisierung
O: Lokalität
A: Ohne abgeschlossene Abstraktion kann nicht strukturiert werden. Strukturierung und Abstraktion sind wiederum Voraussetzung für die Hierarchisierung.

### Aufgabe
Typ: truefalse
F: Ein Modell soll die Wirklichkeit möglichst genau und vollständig abbilden.
L: false
A: Ein Modell ist eine bewusste **Verkürzung** durch Selektion oder Verdichtung. Die Kunst liegt nicht in der genauesten, sondern in der passenden Detailstufe.

### Aufgabe
Typ: checkbox
F: Welche der folgenden Eigenschaften machen ein Modell aus?
O: *Abbildung
O: *Verkürzung
O: *Pragmatik
O: Vollständigkeit
O: Formalisierung
A: Ein Modell bildet ein System ab, vereinfacht es bewusst und ist immer für einen bestimmten Zweck gemacht.

### Aufgabe
Typ: radio
F: Wie lautet die Forderung nach Einfachheit im Prinzip "Bindung und Kopplung"?
O: Kopplungen maximieren, Bindungen minimieren
O: *Kopplungen minimieren, Bindungen maximieren
O: Kopplungen und Bindungen gleichermaßen minimieren
O: Kopplungen und Bindungen gleichermaßen maximieren
A: Innerhalb einer Komponente stark zusammengehörig, zwischen den Komponenten möglichst wenig Abhängigkeit. Dieselbe Aussage findet sich später in SOLID wieder.

### Aufgabe
Typ: fillblank
F: Ein Modell, das eine bereits bestehende Wirklichkeit beschreibt, ist {{präskriptiv|*deskriptiv|normativ}}. Ein Modell, das als Vorbild für ein noch nicht existierendes System dient, ist {{*präskriptiv|deskriptiv|iterativ}}.
A: Die XML-Aufgabe der letzten Klausur war deskriptive Modellbildung — eine vorhandene Struktur wird beschrieben. Die beiden Textaufgaben waren präskriptiv.

### Aufgabe
Typ: radio
F: Auf welcher Abstraktionsebene arbeitest du, wenn du ein Klassendiagramm zeichnest?
O: Exemplar-Ebene
O: *Typ-Ebene
O: Meta-Ebene
O: Instanz-Ebene
A: Die Typ-Ebene beschreibt Vorlagen. Ein Objektdiagramm mit konkreten Werten liegt auf der Exemplar-Ebene, die UML-Spezifikation selbst auf der Meta-Ebene.

### Aufgabe
Typ: block
F: Ordne die Modellierungswerkzeuge der jeweiligen Dimension der Basiskonzepte zu.
S: Statik
S: Dynamik
S: Logik
K: Klassendiagramm -> Statik
K: Objektdiagramm -> Statik
K: Zustandsautomat -> Dynamik
K: Aktivitätsdiagramm -> Dynamik
K: Petrinetz -> Dynamik
K: Entscheidungstabelle -> Logik
K: Entscheidungsbaum -> Logik
A: Statik beschreibt, was über die Zeit unveränderlich ist, Dynamik die Abläufe, Logik die Regelwerke.

### Aufgabe
Typ: truefalse
F: Das Prinzip der Verbalisierung besagt, dass sich bei der Namensgebung zeigt, ob die gewählte Struktur überhaupt stimmt.
L: true
A: Findest du für eine Klasse keinen sauberen Namen, ist meist nicht der Name das Problem, sondern die Klasse.
H1: Denk an das Vorgesetzten-Beispiel aus der Vorlesung.

### Aufgabe
Typ: checkbox
F: Welche Aussagen zum Systembegriff nach Balzert sind korrekt?
O: *Ein System ist ein Ausschnitt aus der realen oder gedanklichen Welt.
O: *Teile, die nicht weiter zerlegt werden sollen, heißen Systemelemente.
O: *Systemkomponenten stehen untereinander in Beziehungen.
O: Ein System muss immer technischer Natur sein.
O: Systemelemente lassen sich stets weiter zerlegen.
A: Ob ein Teil ein Systemelement ist, ist eine Entscheidung des Modellierers — nicht eine Eigenschaft der Welt.

### Aufgabe
Typ: radio
F: Was ist der Kern des Prinzips der Hierarchisierung?
O: Zerlegung in Teile mit definierten Schnittstellen
O: *Strukturierung mit einer Rangordnung zwischen über- und untergeordneten Teilen
O: Verbergen von Informationen nach außen
O: Räumliche Nähe zusammengehöriger Elemente
A: Hierarchisierung ist ein Spezialfall der Strukturierung. Vererbung, verschachtelte Pakete und XML-Bäume sind Hierarchien.

## Die Klasse
Notation, Klassennamen, Attribute und die Entscheidung zwischen Klasse, Attribut und Datentyp.

### Aufgabe
Typ: radio
F: In welcher Form soll ein Klassenname nach Balzert stehen?
O: Substantiv im Plural
O: *Substantiv im Singular
O: Verb im Infinitiv
O: Adjektiv mit nachgestelltem Substantiv im Plural
A: Die Klasse beschreibt ein einzelnes Objekt, nicht die Menge. Die Menge entsteht über die Multiplizität an der Assoziation.

### Aufgabe
Typ: checkbox
F: Was spricht dafür, einen Begriff als **eigene Klasse** und nicht als Attribut zu modellieren?
O: *Er besitzt eine eigene Objektidentität.
O: *Er existiert unabhängig von anderen Objekten.
O: *Der Zugriff ist grundsätzlich in beide Richtungen möglich.
O: Seine Existenz hängt vom übergeordneten Objekt ab.
O: Er hat im System eine untergeordnete Bedeutung.
A: Der Kerntest lautet: Könnte dieses Ding allein in der Welt stehen und hätte trotzdem Bedeutung? Dann Klasse, sonst Attribut.

### Aufgabe
Typ: truefalse
F: Eine 1:1-Assoziation zwischen zwei Klassen ist in der Regel ein Hinweis darauf, dass eigentlich ein strukturierter Datentyp gemeint ist.
L: true
A: Beispiel Kunde und Kontaktdaten: Der Kunde *hat* ein Attribut vom Typ KontaktT. Zwei Tabellen mit Fremdschlüssel wären hier unnötiger Aufwand.
H1: Ausnahme: Die zweite Klasse hat eigene Attribute *und* eigene Assoziationen zu weiteren Klassen.

### Aufgabe
Typ: radio
F: Was bedeutet ein Schrägstrich vor einem Attributnamen, also `/alter: Integer`?
O: Das Attribut ist privat.
O: Das Attribut ist ein Klassenattribut.
O: *Das Attribut wird berechnet und nicht gespeichert.
O: Das Attribut ist optional.
A: Abgeleitete Attribute erkennst du im Aufgabentext an Formulierungen wie "ergibt sich aus", "wird berechnet aus" oder "die Summe aller".

### Aufgabe
Typ: radio
F: Wie wird ein Klassenattribut notiert — also ein Attribut, das für alle Objekte denselben Wert hat?
O: kursiv
O: *unterstrichen
O: in geschweiften Klammern
O: mit vorangestelltem Schrägstrich
A: Ein Klassenattribut liegt vor, wenn alle Objekte denselben Wert besitzen oder wenn Informationen über die Gesamtheit der Objekte modelliert werden.

### Aufgabe
Typ: fillblank
F: Die Sichtbarkeit `private` wird mit dem Zeichen {{+|*-|#|~}} notiert, `protected` mit {{+|-|*#|~}} und `public` mit {{*+|-|#|~}}.
A: Sichtbarkeiten sind die Notationsform des Geheimnisprinzips. Die Tilde `~` steht für package.

### Aufgabe
Typ: block
F: Ordne die Notationselemente ihrer Bedeutung zu.
S: Attribut-Eigenschaft
S: Stereotyp
S: Sonderkennzeichnung
K: {readOnly} -> Attribut-Eigenschaft
K: {id} -> Attribut-Eigenschaft
K: {unique} -> Attribut-Eigenschaft
K: «enumeration» -> Stereotyp
K: «datatype» -> Stereotyp
K: Unterstreichung -> Sonderkennzeichnung
K: Kursivschrift -> Sonderkennzeichnung
A: Eigenschaftswerte stehen in geschweiften Klammern hinter dem Attribut, Stereotypen in Doppelspitzklammern über dem Klassennamen.

### Aufgabe
Typ: truefalse
F: In einem Urlaubsantragssystem sind "Mitarbeiter" und "Vorgesetzter" sinnvoll als zwei Unterklassen von "Person" zu modellieren.
L: false
A: Das sind **Rollen**, keine Klassen. Vorgesetzte sind auch Mitarbeiter und wollen selbst Urlaub nehmen. Richtig ist eine reflexive Assoziation auf Person mit Rollennamen an beiden Enden.
H1: Prüfe: Kann der Vorgesetzte in diesem Modell selbst einen Antrag stellen?

### Aufgabe
Typ: checkbox
F: Welche Klassen haben in einem fachlichen Analysemodell nach Balzert **nichts** verloren?
O: *Klassen, die die Benutzungsoberfläche modellieren
O: *Klassen, die nur Objektmengen verwalten
O: *Klassen, die Entwurfs- oder Implementierungsdetails abbilden
O: Klassen, die eine abstrakte Oberklasse bilden
O: Klassen mit nur einem einzigen Attribut
A: Eine Klasse "Mitgliederliste" neben "Mitglied" ist überflüssig — die Liste *ist* bereits die Multiplizität an der Assoziation.

### Aufgabe
Typ: radio
F: Im Aufgabentext steht: "Der Status kann die Werte offen, in Bearbeitung oder abgeschlossen annehmen." Wie modellierst du das?
O: als drei Unterklassen
O: als drei Boolean-Attribute
O: *als Enumeration
O: als String-Attribut mit Multiplizität [1..3]
A: Endliche, feste Wertemengen werden zu Enumerationen. Ein String wäre zu unspezifisch — die Enumeration sagt der späteren Oberfläche, dass ein Dropdown gebraucht wird.

### Aufgabe
Typ: fillblank
F: Der Test, ob ein Attribut in einer Klasse richtig sitzt, lautet: Muss es auch dann zu jedem Objekt gehören, wenn man die Klasse völlig {{isoliert;isolliert;getrennt}} von allen anderen Klassen betrachtet?
A: Der Isolationstest. Fällt die Antwort negativ aus, gehört das Attribut vermutlich an eine Assoziation — der Klassiker ist die Menge im Warenkorb.
H1: Das Gegenteil von "im Zusammenhang mit anderen".

## Beziehungen zwischen Klassen
Assoziationen, Multiplizitäten, Vererbung sowie Aggregation und Komposition.

### Aufgabe
Typ: radio
F: An welchem Ende der Beziehung steht die Raute bei Aggregation und Komposition?
O: *am Ganzen
O: am Teil
O: an beiden Enden
O: je nach Leserichtung wechselnd
A: Die Raute markiert immer das Ganze. Das ist eine der häufigsten Verwechslungen in Klausurdiagrammen.

### Aufgabe
Typ: truefalse
F: Die Aggregation wird durch eine ausgefüllte, schwarze Raute dargestellt.
L: false
A: Umgekehrt: Die **Aggregation** hat eine weiße (nicht ausgefüllte) Raute, die **Komposition** eine schwarze.

### Aufgabe
Typ: checkbox
F: Welche Bedingungen müssen für eine Komposition erfüllt sein?
O: *Es liegt eine "ist Teil von"-Beziehung vor.
O: *Die Multiplizität am Ganzen beträgt höchstens 1.
O: *Die Lebensdauer der Teile ist an die des Ganzen gebunden.
O: Ein Teil kann gleichzeitig zu mehreren Ganzen gehören.
O: Das Teil und das Ganze sind gleichrangig.
A: Kann ein Teil zu mehreren Ganzen gehören, handelt es sich höchstens um eine shared aggregation — also die weiße Raute.

### Aufgabe
Typ: radio
F: Welcher Test entscheidet am schnellsten, ob eine Komposition vorliegt?
O: Ist das Ganze wichtiger als das Teil?
O: *Verschwindet das Teil sinnvollerweise, wenn das Ganze gelöscht wird?
O: Hat das Teil mehr Attribute als das Ganze?
O: Ist das Teil im Aufgabentext zuerst genannt?
A: Der Löschtest. Steht im Aufgabentext ein explizites Löschverhalten ("wird der Kunde entfernt, wird auch seine Akte vernichtet"), ist die Sache entschieden.

### Aufgabe
Typ: block
F: Ordne jedem Sachverhalt die passende Beziehungsart zu.
S: Komposition
S: Aggregation
S: Einfache Assoziation
K: Bestellung und Bestellposition -> Komposition
K: Sparkonto und Kontobewegung -> Komposition
K: Auto und Motor -> Komposition
K: Web-Auftritt und Web-Seite -> Aggregation
K: Fahrlehrer und Ausbildungseinheit -> Einfache Assoziation
K: Kunde und Sachbearbeiter -> Einfache Assoziation
A: Eine Web-Seite kann in mehreren Auftritten referenziert werden, gehört also zu mehreren Ganzen. Balzert rät: im Zweifel immer die einfache Assoziation.
H1: Frage bei jedem Paar: Kann das Teil zu mehreren Ganzen gehören?

### Aufgabe
Typ: radio
F: Im Text stehen drei Arten eines Begriffs, die sich in ihren Attributen **nicht** unterscheiden. Was modellierst du?
O: eine Vererbungshierarchie mit abstrakter Oberklasse
O: *eine Enumeration
O: drei Kompositionen
O: eine Assoziationsklasse
A: Vererbung liegt nur vor, wenn die Unterklassen eigene Attribute, Operationen oder Assoziationen mitbringen. Sonst ist es eine Aufzählung von Ausprägungen.

### Aufgabe
Typ: truefalse
F: Eine abstrakte Klasse wird durch einen kursiv gesetzten Klassennamen gekennzeichnet.
L: true
A: Alternativ ist die Eigenschaft `{abstract}` erlaubt. Die Oberklasse wird abstrakt, wenn es kein Objekt gibt, das keiner ihrer Unterklassen angehört.

### Aufgabe
Typ: fillblank
F: Steht im Aufgabentext "alle Versuche werden gespeichert", modellierst du eine {{Momentaufnahme|*Historie|Aggregation}} und setzt die Multiplizität auf {{0..1|1|*}}.
A: Balzerts erste Prüffrage zur Multiplizität: Schnappschuss oder Historie? Bei einem Schnappschuss wird die alte Beziehung gelöst, bevor eine neue entsteht.

### Aufgabe
Typ: checkbox
F: In welchen Fällen ist ein Rollenname an der Assoziation zwingend nötig?
O: *bei reflexiven Assoziationen
O: *wenn eine Klasse in verschiedenen Assoziationen verschiedene Rollen spielt
O: *wenn zwischen zwei Klassen mehrere Assoziationen bestehen
O: bei jeder Komposition
O: bei jeder Vererbungsbeziehung
A: Je allgemeiner der Klassenname, desto wichtiger der Rollenname. Vererbung trägt keine Rollennamen.

### Aufgabe
Typ: radio
F: Ein Artikel liegt in einem Warenkorb, und dabei ist eine Menge zu speichern. Wo gehört das Attribut "menge" hin?
O: in die Klasse Artikel
O: in die Klasse Warenkorb
O: *an die Assoziation zwischen beiden, als Assoziationsklasse oder aufgelöste Zwischenklasse
O: in eine Enumeration
A: Ein Artikel hat für sich genommen keine Menge — die entsteht erst in Bezug auf einen konkreten Warenkorb. Das ist der Isolationstest in Anwendung.

### Aufgabe
Typ: truefalse
F: Bei einer Vererbung erbt die Unterklasse nur die Attribute und Operationen der Oberklasse, nicht aber deren Assoziationen.
L: false
A: Vererbt werden Attribute, Operationen **und** Assoziationen. Hat "Person" eine Assoziation zu "Anschrift", haben Kunde und Mitarbeiter sie automatisch mit.

### Aufgabe
Typ: radio
F: Der Text sagt: "Eine Sonderfahrt ist eine besondere Form der Fahrstunde." Wo hängt Sonderfahrt in der Hierarchie?
O: direkt unter der abstrakten Oberklasse Ausbildungseinheit
O: *unter Fahrstunde
O: als eigenständige Klasse ohne Vererbung
O: als Enumeration innerhalb von Fahrstunde
A: Die Formulierung nennt die Hierarchiestufe direkt. Hängt man alle nebeneinander, muss das Attribut "strecke" doppelt modelliert werden — genau die Redundanz, die Vererbung vermeiden soll.
H1: Hat eine Sonderfahrt eine gefahrene Strecke?

## XML zum Klassendiagramm
Die sechs Übersetzungsregeln vom XML-Dokument zum UML-Klassendiagramm.

### Aufgabe
Typ: radio
F: Ein Element `<raeume>` enthält ausschließlich mehrere `<raum>`-Elemente. Wie modellierst du `<raeume>`?
O: als eigene Klasse mit Komposition zu Raum
O: als Attribut der übergeordneten Klasse
O: *gar nicht — es ist ein Sammelelement
O: als Enumeration
A: Sammelelemente im Plural sind reine XML-Syntax. Die Sammlung *ist* die Multiplizität. Wer daraus eine Klasse macht, verliert doppelt: überflüssige Klasse plus fehlende Multiplizität.

### Aufgabe
Typ: truefalse
F: Ob eine Information als XML-Attribut in der Anfangsmarkierung oder als einfaches Kindelement notiert ist, macht für das Klassendiagramm keinen Unterschied.
L: true
A: Beides wird zu einem Attribut. Das Übersehen der XML-Attribute in der Anfangsmarkierung ist einer der häufigsten Fehler — dort steckt oft die Hälfte aller Attribute.

### Aufgabe
Typ: radio
F: Ein `<vortrag>`-Element trägt das Attribut `referent="mm"`, und weiter oben im Dokument steht `<referent kuerzel="mm">`. Wie modellierst du das?
O: als String-Attribut von Vortrag
O: *als Assoziation zwischen Vortrag und Referent
O: als Komposition von Vortrag zu Referent
O: als Enumeration mit allen Kürzeln
A: Das ist ein Verweis, keine Verschachtelung. Wer ihn als String modelliert, hat das Dokument abgeschrieben statt die Struktur verstanden.

### Aufgabe
Typ: fillblank
F: Physische Verschachtelung in XML wird zur {{Assoziation|*Komposition|Aggregation}}, ein Verweis über eine ID wird zur {{*Assoziation|Komposition|Vererbung}}.
A: Der Merksatz des Kapitels. Verschachtelung erfüllt die Kompositionskriterien: genau ein Elternelement, und beim Löschen verschwindet der ganze Teilbaum.

### Aufgabe
Typ: block
F: Ordne jedes XML-Konstrukt seiner UML-Entsprechung zu.
S: Klasse
S: Attribut
S: Multiplizität
S: Wird nicht modelliert
K: Element, das mehrfach vorkommen kann -> Klasse
K: XML-Attribut in der Anfangsmarkierung -> Attribut
K: einfaches Kindelement ohne eigene Kinder -> Attribut
K: dasselbe Element mehrfach hintereinander -> Multiplizität
K: Sammelelement im Plural -> Wird nicht modelliert
A: Fünf der sechs Übersetzungsregeln in einer Übersicht. Die sechste betrifft Verweise über IDs, die zu Assoziationen werden.

### Aufgabe
Typ: radio
F: In einer DTD steht hinter einem Element ein `+`. Welche UML-Multiplizität entspricht dem?
O: 0..1
O: 0..*
O: *1..*
O: genau 1
A: Fragezeichen bedeutet optional (0..1), Plus mindestens einmal (1..*), Stern beliebig oft (0..*). Im XML-Schema heißen die Angaben minOccurs und maxOccurs.

### Aufgabe
Typ: truefalse
F: Bei gleichartiger Verschachtelung — etwa `<kapitel>` innerhalb von `<kapitel>` — beträgt die Multiplizität am Ganzen 1.
L: false
A: Sie beträgt **0..1**. Sonst müsste jedes Kapitel in einem anderen Kapitel stecken und es gäbe kein oberstes. Balzert behandelt das als Muster "Stückliste".
H1: Denk an das oberste Element des Baums.

### Aufgabe
Typ: checkbox
F: Ein Element `<qualifikation>` kommt innerhalb von `<mechaniker>` zweimal vor und enthält jeweils nur Text. Welche Modellierungen sind vertretbar?
O: *Attribut `qualifikation: String [1..*]` in der Klasse Mechaniker
O: eine eigene Klasse Qualifikation mit Komposition
O: eine Enumeration mit allen im Dokument vorkommenden Werten
O: *Attribut mit Multiplizität, alternativ eine eigene Klasse, falls Qualifikationen zentral verwaltet würden
A: Da das Element keine eigenen Eigenschaften trägt, ist das Attribut mit Multiplizität die schlankere Lösung. Eine eigene Klasse wäre nur bei zentraler Verwaltung sinnvoll — und das müsste der Aufgabentext hergeben.

## Zustandsautomaten
Zustände, Transitionen, Ereignisarten und hierarchische Automaten.

### Aufgabe
Typ: radio
F: Woran erkennst du, dass ein Sachverhalt einen Zustandsautomaten und kein Aktivitätsdiagramm verlangt?
O: Es kommen mehrere Rollen vor.
O: *Dieselbe Eingabe wirkt je nach Vorgeschichte unterschiedlich.
O: Der Ablauf enthält parallele Schritte.
O: Es gibt mehr als fünf Schritte.
A: Beispiel Rolladensteuerung: Der Taster "Hoch" fährt im Normalbetrieb den Rolladen hoch und erhöht im Einstellungsmodus die Stundenzahl.

### Aufgabe
Typ: truefalse
F: Zustandsnamen sollen möglichst als Verb formuliert werden, etwa "ausleihen".
L: false
A: Ein Zustandsname soll kein Verb sein, sondern wenn möglich ein Adjektiv oder Partizip — also "ausgeliehen". Ein Zustand beschreibt, wie das System *ist*, nicht was es *tut*.

### Aufgabe
Typ: radio
F: In welcher Reihenfolge stehen die Bestandteile einer Transitionsbeschriftung?
O: Wächter, Ereignis, Aktion
O: *Ereignis, Wächter in eckigen Klammern, Aktion nach Schrägstrich
O: Aktion, Ereignis, Wächter
O: Ereignis, Aktion, Wächter in geschweiften Klammern
A: Alle drei Bestandteile sind optional. Eine Transition ganz ohne Beschriftung ist ein implizites Ereignis — sie feuert, wenn die Verarbeitung im Zustand beendet ist.

### Aufgabe
Typ: checkbox
F: Welche Aussagen zu entry, do und exit sind korrekt?
O: *`entry` wird beim Betreten des Zustands ausgeführt.
O: *`do` läuft, solange das System im Zustand ist.
O: *`exit` wird beim Verlassen ausgeführt, unabhängig davon, über welche Transition.
O: `do` wird nur beim ersten Betreten ausgeführt.
O: `entry` ersetzt alle eingehenden Transitionen.
A: Eine `entry`-Aktion sagt dasselbe aus, als würde jeder eingehende Übergang diese Aktion tragen. Soll etwas nur bei einem bestimmten Übergang passieren, gehört es an die Transition.

### Aufgabe
Typ: fillblank
F: Eine Bedingung, die wahr wird, notierst du mit {{*when|after|until}}, eine verstrichene Zeitspanne mit {{when|*after|during}}.
A: Beispiele: `when (Kontostand < 0)` und `after (10 Sekunden)`.

### Aufgabe
Typ: radio
F: Worin unterscheidet sich eine Aktion von einer Aktivität?
O: Aktionen stehen an Transitionen, Aktivitäten an Zuständen — sonst kein Unterschied.
O: *Eine Aktion braucht im Idealfall keine Zeit und wird immer vollständig ausgeführt; eine Aktivität dauert und kann vorzeitig beendet werden.
O: Eine Aktivität ist immer nebenläufig, eine Aktion nie.
O: Aktionen sind optional, Aktivitäten verpflichtend.
A: Deshalb gehört "Ergebnis speichern" als Aktion an die Transition, während "Epoche trainieren" eine `do`-Aktivität im Zustand ist.

### Aufgabe
Typ: radio
F: Im Aufgabentext steht: "Der Anwender kann den Vorgang jederzeit abbrechen." Welche Modellierung ist die eleganteste?
O: eine Transition vom Anfangszustand zum Endzustand
O: je eine Transition von jedem einzelnen Zustand zum Endzustand
O: *ein zusammengesetzter Zustand mit einem Gruppenübergang von seiner Grenze zum Endzustand
O: eine `exit`-Aktion in jedem Zustand
A: Aus fünf Pfeilen wird einer, und das Diagramm bleibt lesbar. Einzelpfeile sind inhaltlich korrekt, nur unruhiger.
H1: Was passiert, wenn mehrere Zustände durch dasselbe Ereignis verlassen werden?

### Aufgabe
Typ: truefalse
F: Ein Kreis mit einem H markiert in einem hierarchischen Zustandsautomaten die flache Historie.
L: true
A: H* steht für die tiefe Historie über alle Verfeinerungsstufen hinweg. Beides merkt sich den zuletzt aktiven Unterzustand.

### Aufgabe
Typ: radio
F: Welches Ziel gibt Balzert für das Aufstellen eines Zustandsautomaten vor?
O: möglichst viele Zustände, um alle Fälle abzudecken
O: *möglichst wenige Zustände
O: genau so viele Zustände wie Ereignisse
O: eine gerade Anzahl von Zuständen
A: Deshalb lohnt es sich, kurze Aktionen an Transitionen zu hängen statt eigene Zustände dafür zu bilden.

### Aufgabe
Typ: checkbox
F: Welche Automatenmodelle vereint der Harel-Automat, den die UML verwendet?
O: *Mealy-Automat — Ausgabe am Zustandsübergang
O: *Moore-Automat — Ausgabe am Zustand
O: Turing-Maschine
O: Kellerautomat
A: Man spricht deshalb von hybriden Zustandsautomaten. Hinzu kommen Hierarchie, Historie und Nebenläufigkeit.

## Aktivitätsdiagramme und Petrinetze
Kontrollstrukturen, Notation, Swimlanes und der formale Unterbau.

### Aufgabe
Typ: radio
F: Was bedeutet der dicke schwarze Balken im Aktivitätsdiagramm?
O: eine Entscheidung zwischen mehreren Wegen
O: *Fork und Join — echte Nebenläufigkeit
O: den Endknoten
O: einen Objektknoten
A: Merksatz: Raute bedeutet Entweder-oder, Balken bedeutet Sowohl-als-auch.

### Aufgabe
Typ: truefalse
F: Ein Join lässt den Kontrollfluss weiterlaufen, sobald der erste eingehende Strang fertig ist.
L: false
A: Der Join **wartet**, bis alle eingehenden Stränge ihr Ende erreicht haben — auch wenn ein Strang eine Minute und ein anderer zehn dauert.

### Aufgabe
Typ: checkbox
F: Welche gehören zu den fünf Kontrollstrukturen nach Balzert?
O: *Sequenz
O: *Auswahl
O: *Wiederholung
O: *Aufruf
O: *Nebenläufigkeit
O: Rekursion
A: Wer programmiert, erkennt hier if, while, Funktionsaufruf und Threads wieder. Rekursion ist ein Sonderfall des Aufrufs, keine eigene Kontrollstruktur der Liste.

### Aufgabe
Typ: radio
F: Wofür werden Aktivitätsbereiche (Swimlanes) eingesetzt?
O: um parallele Abläufe zu kennzeichnen
O: *um Aktionen den ausführenden Akteuren oder Systemen zuzuordnen
O: um Bedingungen zu notieren
O: um Zeitabschnitte darzustellen
A: Sobald der Aufgabentext Rollen nennt und ihnen Tätigkeiten zuordnet, sind Swimlanes die naheliegende Modellierung.

### Aufgabe
Typ: block
F: Ordne jedes Symbol dem Diagrammtyp zu, für den es charakteristisch ist.
S: Aktivitätsdiagramm
S: Zustandsautomat
S: Petrinetz
K: Fork- und Join-Balken -> Aktivitätsdiagramm
K: Swimlane -> Aktivitätsdiagramm
K: entry / do / exit -> Zustandsautomat
K: Wächter in eckigen Klammern -> Zustandsautomat
K: Stelle als Kreis -> Petrinetz
K: Marke -> Petrinetz
A: Wächter kommen auch im Aktivitätsdiagramm an der Raute vor — charakteristisch sind sie aber für die Transitionsbeschriftung im Zustandsautomaten.

### Aufgabe
Typ: radio
F: Was ist der wesentliche Vorteil von Petrinetzen gegenüber anderen Verhaltensmodellen?
O: Sie sind für Fachanwender leichter lesbar.
O: *Sie sind mathematisch fundiert und erlauben den formalen Nachweis von Deadlock-Freiheit.
O: Sie benötigen weniger Symbole.
O: Sie lassen sich direkt in Quellcode übersetzen.
A: Bei einem übersichtlichen Ablauf sieht man Deadlocks mit bloßem Auge — bei komplexen nebenläufigen Prozessen nicht mehr.

### Aufgabe
Typ: fillblank
F: In einem Petrinetz werden {{*Stellen|Zustände|Knoten}} und Transitionen immer {{parallel|*abwechselnd|beliebig}} durch gerichtete Kanten verbunden.
A: Eine Stelle ist nie direkt mit einer Stelle verbunden, eine Transition nie direkt mit einer Transition.

### Aufgabe
Typ: truefalse
F: Eine `if`-Anweisung im Quellcode sollte im Aktivitätsdiagramm als Entscheidungsknoten modelliert werden.
L: false
A: Man modelliert nicht auf der Ebene des Quellcodes, sondern semantische Prozesse. Sonst würden die Diagramme so groß, dass es einfacher wäre, den Code zu lesen.
H1: Denk an das Kriterium: Wann hilft das Modell dem Verständnis?

### Aufgabe
Typ: radio
F: Wie viele Use Cases sind für ein mittleres System von 1.000 bis 10.000 Personentagen als Faustregel angemessen?
O: 5 bis 10
O: 10 bis 15
O: *30 bis 60
O: 150 bis 300
A: Kleine Systeme kommen mit 10 bis 15 aus, große mit 80 bis 150. Ein Use-Case-Diagramm ist bewusst grob.

## Entscheidungstabellen und Logik
Aufbau, Vollständigkeit, Konsolidierung und regelbasierte Systeme.

### Aufgabe
Typ: radio
F: Wie viele Regeln enthält eine formal vollständige Entscheidungstabelle mit vier Bedingungen?
O: 4
O: 8
O: *16
O: 24
A: Bei n Bedingungen sind es 2 hoch n Kombinationen. Balzert empfiehlt, bei weniger als fünf Bedingungen zunächst die vollständige Tabelle anzulegen und erst danach zu optimieren.

### Aufgabe
Typ: checkbox
F: Aus welchen vier Quadranten besteht eine Entscheidungstabelle?
O: *Bedingungen
O: *Bedingungsanzeiger
O: *Aktionen
O: *Aktionsanzeiger
O: Auswertungsvektor
A: Der Auswertungsvektor entsteht erst bei der Anwendung — er ist kein Bestandteil der Tabelle.

### Aufgabe
Typ: truefalse
F: Eine Entscheidungstabelle legt fest, in welcher Reihenfolge die Bedingungen geprüft werden.
L: false
A: Eine Entscheidungstabelle ist **kein Algorithmus**, sondern eine Menge aussagenlogischer Regeln. Genau das ist ihr Vorteil in der Definitionsphase — der Entscheidungsbaum gibt diese Offenheit auf.

### Aufgabe
Typ: fillblank
F: Unterscheiden sich zwei Regeln mit identischen Aktionen nur in einer einzigen Bedingungszeile, werden sie zusammengefasst und der abweichende Anzeiger durch einen {{Nullwert|*Irrelevanzanzeiger|Platzhalter}} ersetzt.
A: Notiert wird er als Strich. Beim Scheck-Beispiel schrumpft die Tabelle so von acht auf vier Regeln.

### Aufgabe
Typ: radio
F: Worin unterscheiden sich formale und inhaltliche Vollständigkeit?
O: *Formal: alle 2^n Kombinationen sind eingetragen. Inhaltlich: alle praktisch möglichen Kombinationen sind aufgeführt.
O: Formal: alle Aktionen sind belegt. Inhaltlich: alle Bedingungen sind belegt.
O: Formal bezieht sich auf die Notation, inhaltlich auf die Sprache.
O: Es handelt sich um Synonyme.
A: Beim Scheck-Beispiel sind zwei der acht Kombinationen fachlich unmöglich: Ohne überschrittene Kreditgrenze kann es keinen Überschreitungsbetrag geben.

### Aufgabe
Typ: checkbox
F: Welche Eigenschaften hat die Else-Regel?
O: *Sie hat keine Bedingungsanzeiger.
O: *Pro Tabelle ist nur eine erlaubt.
O: *Sie macht aus einer unvollständigen eine vollständige Tabelle.
O: Sie muss immer ganz links stehen.
O: Sie ersetzt alle Aktionsanzeiger.
A: Empfohlen wird die Position ganz rechts, zwingend ist sie nicht.

### Aufgabe
Typ: radio
F: Was gilt für eine Mehrtreffer-Tabelle?
O: Nur die erste zutreffende Regel wird ausgeführt.
O: *Alle Regeln müssen geprüft werden; die Aktionen aller zutreffenden Regeln werden ausgeführt, sofern sie sich nicht widersprechen.
O: Sie darf keine Irrelevanzanzeiger enthalten.
O: Sie ist immer inhaltlich unvollständig.
A: Bei einer Eintreffer-Tabelle schließen sich die Bedingungsanzeiger gegenseitig aus — hat man eine gültige Regel gefunden, ist man fertig.

### Aufgabe
Typ: block
F: Ordne jeder Logikform ihren Gegenstand zu.
S: Aussagenlogik
S: Prädikatenlogik
S: Temporale Logik
K: Verknüpfung elementarer Aussagen -> Aussagenlogik
K: Prüfung auf Widerspruchsfreiheit von Anforderungen -> Aussagenlogik
K: Quantoren wie "für alle" und "es gibt" -> Prädikatenlogik
K: Beziehungen zwischen Objekten -> Prädikatenlogik
K: Aussagen, deren Wahrheitswert sich mit der Zeit ändert -> Temporale Logik
K: CTL und LTL -> Temporale Logik
A: Der praktische Nutzen jeder Formalisierung ist derselbe: Präzisierung und Analysierbarkeit.

### Aufgabe
Typ: radio
F: Wie heißt in einem regelbasierten System die Menge aller Regeln, deren Bedingungsteil aktuell erfüllt ist?
O: Faktenbasis
O: *Konfliktmenge
O: Regelbasis
O: Auswertungsvektor
A: Die eigentliche Schwierigkeit regelbasierter Systeme liegt nicht in den Regeln, sondern in der Konfliktauflösung — etwa "speziell vor allgemein" oder "neu vor alt".
H1: Der Begriff beschreibt, dass mehrere Regeln gleichzeitig anwendbar sind.

## Requirements Engineering
Verträge, Stakeholder, Anforderungsarten und Aufwandsschätzung.

### Aufgabe
Typ: radio
F: Worin unterscheiden sich Lastenheft und Pflichtenheft?
O: Das Lastenheft ist technischer, das Pflichtenheft fachlicher.
O: *Das Lastenheft beschreibt aus Auftraggebersicht, was gefordert wird; das Pflichtenheft aus Auftragnehmersicht, was geliefert wird.
O: Das Pflichtenheft entsteht vor dem Lastenheft.
O: Sie unterscheiden sich nur im Namen.
A: Das Pflichtenheft ist eine Verfeinerung und Präzisierung des Lastenhefts und in der Regel Anlage zum Festpreisangebot.

### Aufgabe
Typ: checkbox
F: Welche Vertragsarten erfordern zwingend eine Leistungsbeschreibung?
O: *Festpreis
O: *Wartung
O: Time and Material
O: Service
A: Bei der Wartung deshalb, weil ein Fehler definitionsgemäß eine Abweichung vom Soll ist. Ohne definiertes Soll lässt sich kein Fehler feststellen.
H1: Was schuldet der Auftragnehmer jeweils — Personal oder ein Gewerk?

### Aufgabe
Typ: truefalse
F: Ein vereinbarter Fertigstellungstermin ist eine funktionale Anforderung.
L: false
A: Das ist eine **Randbedingung**. "Funktional" heißt schlicht: Funktion im Sinne von Feature.

### Aufgabe
Typ: radio
F: Was kennzeichnet Basismerkmale im Kano-Modell?
O: Sie werden explizit gefordert und steigern die Zufriedenheit proportional.
O: *Sie sind unterbewusst und selbstverständlich — fehlen sie, ist das Projekt gefährdet.
O: Sie begeistern, wenn sie vorhanden sind, werden aber nicht vermisst.
O: Sie betreffen ausschließlich nicht-funktionale Anforderungen.
A: Niemand sagt dir, dass beim Speichern keine Daten verloren gehen sollen. Deshalb musst du Basismerkmale selbst mitdenken.

### Aufgabe
Typ: block
F: Ordne jede Anforderung ihrer Art zu.
S: Funktionale Anforderung
S: Nicht-funktionale Anforderung
S: Randbedingung
K: Das System muss Bestellungen erfassen können. -> Funktionale Anforderung
K: Der Sachbearbeiter kann Kunden anlegen. -> Funktionale Anforderung
K: Die Antwortzeit liegt unter zwei Sekunden. -> Nicht-funktionale Anforderung
K: Das System ist barrierefrei bedienbar. -> Nicht-funktionale Anforderung
K: Als Datenbank ist PostgreSQL vorgeschrieben. -> Randbedingung
K: Das System läuft im unbeaufsichtigten Dauerbetrieb. -> Randbedingung
A: Technische Vorgaben sind als Randbedingung legitim, weil sie eine echte Restriktion des Auftraggebers sind — keine vorweggenommene Lösungsentscheidung.

### Aufgabe
Typ: radio
F: Welches Qualitätskriterium für Anforderungen gilt als das härteste?
O: verständlich
O: *prüfbar
O: notwendig
O: klassifizierbar
A: Eine Anforderung, für die sich kein Abnahmekriterium formulieren lässt, ist keine Anforderung, sondern ein Wunsch. "Benutzerfreundlich" ist nicht prüfbar, "unter 90 Sekunden pro Neukunde" schon.

### Aufgabe
Typ: fillblank
F: In einer Anforderungsschablone kennzeichnet {{*muss|sollte|wird}} eine rechtlich verbindliche Pflicht, {{muss|*sollte|wird}} einen Wunsch und {{muss|sollte|*wird}} eine Absichtserklärung für die Zukunft.
A: Bei einem Festpreisprojekt entscheidet diese Wortwahl darüber, was eingeklagt werden kann.

### Aufgabe
Typ: checkbox
F: Welche Schätzverfahren zählen zu den algorithmischen Verfahren?
O: *Function-Points-Methode
O: *COCOMO II
O: Analogiemethode
O: Wideband-Delphi
O: Bottom-up-Methode
A: Analogie, Prozentsatz, Expertenschätzung und Bottom-up beruhen auf Vergleich und Erfahrung. Function Points und COCOMO II rechnen aus früh bekannten Größen.

### Aufgabe
Typ: truefalse
F: Die Anforderungen an ein System stammen in der Regel vom Auftraggeber, der das Budget freigibt.
L: false
A: Der Auftraggeber ist häufig nur der Projektsponsor. Die Anforderungen kommen von den **Stakeholdern**: Stakeholder haben Belange, und aus Belangen ergeben sich Anforderungen.

### Aufgabe
Typ: radio
F: Was bezeichnet adaptive Wartung?
O: die Behebung aufgetretener Fehler
O: *die Anpassung der Software an ihre sich verändernde Umgebung
O: die Erweiterung um neue Features
O: den laufenden Betrieb der Software
A: Software altert nicht — aber ihr Kontext erneuert sich permanent: Betriebssystemversionen, Frameworks, Datenbanken.

### Aufgabe
Typ: radio
F: Ein Kunde verlangt einen Festpreis, es liegen aber noch keine Anforderungen vor. Was ist das sinnvollste Vorgehen?
O: den Kunden fragen, welches Budget er sich vorstellt
O: eine grobe Schätzung abgeben und später nachverhandeln
O: *die Definitionsphase separat beauftragen lassen und danach über den bekannten Phasenanteil auf das Gesamtvolumen hochrechnen
O: den Auftrag ablehnen
A: Man dreht den Spieß nicht um. Man sagt: Ohne Information kann ich keine Aussage zum Preis machen — und teilt das Projekt.
H1: Welchen Wert brauchst du, damit die Prozentsatzmethode überhaupt anwendbar wird?

## Scrum und Prozessmodelle
Cynefin, Rollen, Meetings und der Vergleich zum Wasserfallmodell.

### Aufgabe
Typ: radio
F: In welchem Cynefin-Bereich wird Scrum ausdrücklich empfohlen?
O: offensichtlich
O: kompliziert
O: *komplex
O: chaotisch
A: Im komplexen Bereich lautet die Handlungsfolge probieren, erkennen, reagieren — man muss erst etwas ausprobieren, um zu verstehen, womit man es zu tun hat. Im chaotischen Bereich hilft kein Prozessmodell.

### Aufgabe
Typ: truefalse
F: Ein Scrum-Projekt lässt sich gut als Festpreisprojekt kalkulieren.
L: false
A: Weil das Backlog ständig verändert wird, steht die endgültige Form der Software erst im Laufe des Projekts fest. Ohne definierten Liefergegenstand ist keine Lieferverpflichtung möglich — abgerechnet wird budgetmäßig.

### Aufgabe
Typ: checkbox
F: Welche drei Säulen trägt Scrum als empirischer Prozess?
O: *Transparenz
O: *Inspektion
O: *Adaption
O: Dokumentation
O: Standardisierung
A: Transparenz schafft die Grundlage, Inspektion ist der Blick darauf, Adaption die Reaktion.

### Aufgabe
Typ: radio
F: Wer legt in Scrum die Reihenfolge fest, in der Backlog Items umgesetzt werden?
O: das Entwicklungsteam
O: *der Product Owner
O: der ScrumMaster
O: die Stakeholder gemeinsam
A: Der Product Owner priorisiert, das Team schätzt. Beide Seiten tun sich erfahrungsgemäß schwer damit, die jeweils andere Autorität zu respektieren.

### Aufgabe
Typ: radio
F: Welche Aussage über den ScrumMaster ist korrekt?
O: Er ist gegenüber dem Team weisungsbefugt.
O: *Er löst Hindernisse, sorgt für die Einhaltung des Prozesses und ist nicht weisungsbefugt.
O: Er priorisiert das Product Backlog.
O: Er schätzt gemeinsam mit dem Team die Story Points.
A: Das ist der zentrale Unterschied zum klassischen Projektleiter. Im Buch heißt er der Change Agent — er treibt den Prozess an, aber er befiehlt nicht.

### Aufgabe
Typ: block
F: Ordne jedes Element seiner Kategorie in Scrum zu.
S: Rolle
S: Meeting
S: Artefakt
K: Product Owner -> Rolle
K: ScrumMaster -> Rolle
K: Entwicklungsteam -> Rolle
K: Sprint Planning -> Meeting
K: Daily Scrum -> Meeting
K: Retrospektive -> Meeting
K: Product Backlog -> Artefakt
K: Increment -> Artefakt
K: Burndown-Diagramm -> Artefakt
A: Das Sprint Backlog ist ebenfalls ein Artefakt, das Sprint Review ein weiteres Meeting.

### Aufgabe
Typ: truefalse
F: Die Sprint Retrospektive findet gemeinsam mit den Stakeholdern statt und betrachtet das entstandene Produkt.
L: false
A: Verwechslung mit dem Review. Merkregel: **Review** schaut auf das **Produkt** und ist öffentlich. **Retrospektive** schaut auf den **Prozess** und ist teamintern.

### Aufgabe
Typ: fillblank
F: Ein Sprint dauert typischerweise zwischen einer und {{zwei|*vier|acht}} Wochen. Ein optimales Scrum-Team besteht laut Buch aus {{drei|fünf|*sieben}} Personen.
A: Sieben Personen: ein ScrumMaster, ein Product Owner, fünf Entwickler.

### Aufgabe
Typ: checkbox
F: Welche Merkmale kennzeichnen das klassische Wasserfallmodell?
O: *Die Phasen werden nacheinander abgeschlossen.
O: *Die Qualitätssicherung findet am Ende statt.
O: *Es gibt eine klare Trennung der Rollen wie Architekt, Entwickler und Tester.
O: Feedback kommt nach jedem Inkrement.
O: Das Team organisiert sich selbst.
A: Der Vorteil bleibt: Ein Wasserfallprojekt lässt sich zum Festpreis anbieten, weil der Liefergegenstand am Anfang definiert ist.

### Aufgabe
Typ: radio
F: Was beschreibt die Definition of Done?
O: den Zeitpunkt, an dem ein Sprint endet
O: *die Vereinbarung darüber, wann ein Backlog Item wirklich fertig ist
O: die Abnahmekriterien des Kunden im Vertrag
O: die Anzahl der Story Points, die ein Team pro Sprint schafft
A: Nicht "programmiert", sondern getestet, integriert, dokumentiert. Wird sie von der Leitung vorgeschrieben, geht das meist nach hinten los — das Team legt sie selbst fest.

## Konfigurationsmanagement mit Git
Versionsbegriff, die vier Orte, Git-Flow und Merging.

### Aufgabe
Typ: radio
F: Was ist in einem Versionsverwaltungssystem eine Version?
O: die Änderung an einer einzelnen Datei
O: *die Gesamtmenge aller Dateien und ihrer jeweiligen Stände zu einem Zeitpunkt
O: eine fortlaufende Nummer, die manuell vergeben wird
O: der Inhalt der Staging Area
A: Git betrachtet Informationen als eine Reihe von Schnappschüssen. Unveränderte Dateien werden aus vorherigen Versionen referenziert.

### Aufgabe
Typ: radio
F: Eine Kollegin sagt, sie habe ihre Änderung committet, aber niemand im Team sieht sie. Woran liegt das?
O: Sie hat die Datei nicht zur Staging Area hinzugefügt.
O: *Der Commit liegt nur im lokalen Repository — sie hat nicht gepusht.
O: Die Datei steht in der .gitignore.
O: Es liegt ein Merge-Konflikt vor.
A: Genau diesen Unterschied zwischen Local und Remote Repository soll man laut Dozent verinnerlicht haben. Konsolenbefehle werden nicht abgefragt.

### Aufgabe
Typ: block
F: Ordne jeden Branch des Git-Flow der Betriebsumgebung zu, auf der er läuft.
S: Entwicklungsumgebung
S: QS-Umgebung
S: Staging-Umgebung
S: Produktivumgebung
K: Feature-Branch -> Entwicklungsumgebung
K: Develop -> QS-Umgebung
K: Release -> Staging-Umgebung
K: Master -> Produktivumgebung
A: Eine Version wandert von links nach rechts: vom Feature-Branch über Develop nach Release als Release Candidate und schließlich in den Master.

### Aufgabe
Typ: truefalse
F: Ein nachträglicher Eintrag in die .gitignore entfernt eine bereits getrackte Datei aus dem Repository.
L: false
A: Die .gitignore gilt nur für **ungetrackte** Dateien. Was einmal im Repository ist, bleibt dort, bis es explizit entfernt wird.

### Aufgabe
Typ: radio
F: Warum darf in einem Release-Branch keine Weiterentwicklung mehr stattfinden?
O: weil er technisch schreibgeschützt ist
O: *weil er stabilisiert werden soll — jede neue Funktion würde den Teststand entwerten und den Release verzögern
O: weil Merges in den Master sonst nicht möglich wären
O: weil er nur Binärdateien enthält
A: Dasselbe gilt für Hotfix-Branches: Dort werden ausschließlich Bugfixes durchgeführt.

### Aufgabe
Typ: fillblank
F: Ein {{*Fast-Forward|Three-Way|Rebase}}-Merge tritt auf, wenn sich am Ursprungszweig seit der Abzweigung nichts geändert hat. Der Regelfall in größeren Teams ist dagegen der {{Fast-Forward|*Three-Way|Squash}}-Merge, bei dem ein zusätzlicher Merge-Commit entsteht.
A: Bei beiden Merge-Arten bleibt die Historie erhalten. Rebase dagegen schreibt sie um.

### Aufgabe
Typ: checkbox
F: Welche Situationen führen typischerweise zu einem Merge-Konflikt?
O: *Änderungen an derselben Datei in verschiedenen Branches
O: *unterschiedliche Änderungen an derselben Zeile
O: ein Commit ohne Commit-Message
O: eine Datei, die in der .gitignore steht
A: Erkennbar sind Konflikte an einer Fehlermeldung beim Merge und an Konfliktmarkierungen in den betroffenen Dateien.

### Aufgabe
Typ: truefalse
F: Binärdateien wie Word- oder Excel-Dokumente lassen sich in Git zwar ablegen, aber die Mechanismen des paralleln Arbeitens und Mergens funktionieren dort nicht.
L: true
A: Bei textuellen Dateien wie Quellcode, LaTeX oder Markdown funktionieren sie dagegen sehr wohl.

### Aufgabe
Typ: radio
F: Welche Kette beschreibt Continuous Integration in ihrer Grundform korrekt?
O: Deployment, Build, Commit, Test
O: *Commit, Build, Unit-Tests, Paketierung, Deployment — mit Feedback in jeder Stufe
O: Commit, Deployment, Review, Test
O: Build, Commit, Merge, Release
A: Der Wert liegt in der Verkürzung der Rückkopplung: Ein Fehler wird Minuten nach dem Commit sichtbar, nicht Wochen später im Testzyklus.

## Testgetriebene Entwicklung
Die drei Gesetze, der Workflow, Metriken und die SOLID-Prinzipien.

### Aufgabe
Typ: radio
F: In welcher Reihenfolge arbeitet man bei TDD?
O: Entwurf, Programmieren, Testen
O: *Entwurf, Test entwickeln, Programmieren
O: Test entwickeln, Entwurf, Programmieren
O: Programmieren, Entwurf, Testen
A: TDD ist im Kern eine Aussage über die Reihenfolge — und darüber, dass der Entwickler selbst testet statt einer separaten Rolle.

### Aufgabe
Typ: truefalse
F: Wer automatisierte Unit-Tests schreibt, betreibt damit TDD.
L: false
A: Unit-Tests sind nicht gleich TDD, aber TDD basiert auf Unit-Tests. Man kann Unit-Tests auch hinterher schreiben — dann ist es kein TDD.

### Aufgabe
Typ: checkbox
F: Welche Aussagen gehören zu den drei Gesetzen des TDD?
O: *Niemals Code programmieren, außer er dient dazu, einen fehlgeschlagenen Test zu fixen.
O: *Niemals mehr Unit-Test-Code schreiben als nötig, um einen fehlschlagenden Test zu erzeugen.
O: *Niemals mehr Produktionscode schreiben als nötig, um den Test zu fixen.
O: Jede Klasse braucht mindestens fünf Testfälle.
O: Tests werden erst nach dem Refactoring geschrieben.
A: Wichtiger Zusatz im zweiten Gesetz: Kompilierungsfehler zählen ebenfalls als Fehler. Dadurch werden die Schritte sehr klein.

### Aufgabe
Typ: radio
F: Wozu dient das Faking, also eine bewusst zu einfache Implementierung wie `return 3`?
O: um Zeit zu sparen
O: *um zu prüfen, ob der Testaufbau überhaupt greift — "teste den Test"
O: um die Metrik der zyklomatischen Komplexität zu senken
O: um Platzhalter für später zu markieren
A: Ein Test, der von Anfang an grün ist, weil er nichts prüft, ist gefährlicher als gar kein Test.
H1: Was wäre schlimmer als eine falsche Implementierung — ein Test, der nie fehlschlägt?

### Aufgabe
Typ: fillblank
F: Der TDD-Workflow lautet {{*Red|Green|Refactor}}, dann Green, dann Refactor. Das Motto dazu heißt: Make it green, then make it {{schnell|*clean|klein}}.
A: Wer nur bis Green geht, produziert genau die Software-Entropie, gegen die TDD antreten soll. Refactor ist nicht optional.

### Aufgabe
Typ: radio
F: Was beschreibt die Triangulation?
O: die Prüfung eines Tests aus drei Perspektiven
O: *das Hinzufügen weiterer Testfälle, bis der Schritt zur Generalisierung gelingt
O: die Aufteilung einer Klasse in drei kleinere
O: die Messung von Kopplung, Kohäsion und Komplexität
A: Man kommt schrittweise von der Konstanten zur allgemeinen Lösung — und in keinem Schritt ist die Software kaputt, weil alle bisherigen Tests mitlaufen.

### Aufgabe
Typ: block
F: Ordne jedem SOLID-Prinzip seine Kernaussage zu.
S: Single Responsibility
S: Open-Closed
S: Liskov
S: Interface Segregation
S: Dependency Inversion
K: Eine Klasse erfüllt genau eine fest definierte Aufgabe. -> Single Responsibility
K: Offen für Erweiterungen, geschlossen für Veränderungen. -> Open-Closed
K: Unterklassen müssen sich anstelle ihrer Basisklasse verwenden lassen. -> Liskov
K: Große Schnittstellen in kleinere aufteilen. -> Interface Segregation
K: Module sollten von Abstraktionen abhängen, nicht voneinander. -> Dependency Inversion
A: Single Responsibility zahlt auf die Kohäsion ein, Dependency Inversion senkt die Kopplung.
H1: Zwei der fünf Prinzipien lassen sich direkt einer Metrik zuordnen.

### Aufgabe
Typ: radio
F: Welches Verhältnis von Kopplung und Kohäsion ist anzustreben?
O: starke Kopplung, starke Kohäsion
O: *schwache Kopplung, starke Kohäsion
O: schwache Kopplung, schwache Kohäsion
O: starke Kopplung, schwache Kohäsion
A: Dieselbe Aussage steht bei Balzert als Prinzip der Bindung und Kopplung — TDD ist eine Technik, um zwei sehr alte Prinzipien im Alltag durchzusetzen.

### Aufgabe
Typ: truefalse
F: Die Herstellkosten machen etwa 20 bis 33 Prozent der Gesamtkosten einer Software aus, der Rest entfällt auf Wartung, Pflege und Betrieb.
L: true
A: Genau deshalb ist jede Maßnahme, die die Wartbarkeit verbessert, hebelwirksam. 20 Prozent Ersparnis bei den Wartungskosten sind doppelt so viel wert wie bei den Herstellkosten.

### Aufgabe
Typ: radio
F: Was misst die McCabe-Metrik?
O: die Anzahl der Abhängigkeiten einer Klasse
O: *die Anzahl unabhängiger Pfade durch ein Stück Code
O: die Anzahl der Zeilen pro Methode
O: den Anteil getesteten Codes
A: Man zählt die Verzweigungspunkte. Eine Methode mit einem if, einer for-Schleife und einem switch mit einem behandelten Fall plus default ergibt den Wert 4.

# Karten
## Karte 1
Prinzipien und Modellbegriff | Selbst bewerten
F: Nenne die acht Prinzipien nach Balzert.
A: Abstraktion, Strukturierung, Bindung und Kopplung, Hierarchisierung, Modularisierung, Geheimnisprinzip, Lokalität, Verbalisierung.

## Karte 2
Prinzipien und Modellbegriff
F: Was sind die drei Eigenschaften eines Modells?
A: **Abbildung** (bildet ein System ab), **Verkürzung** (vereinfacht durch Selektion oder Verdichtung), **Pragmatik** (ist immer für einen Zweck gemacht).

## Karte 3
Prinzipien und Modellbegriff
F: Deskriptiv oder präskriptiv — was ist der Unterschied?
A: Deskriptive Modelle beschreiben eine bestehende Wirklichkeit. Präskriptive Modelle sind Vorbild für ein noch nicht existierendes System.

## Karte 4
Prinzipien und Modellbegriff
F: Welche drei Dimensionen haben die Basiskonzepte, und welches Werkzeug gehört jeweils dazu?
A: **Statik** (Klassendiagramm), **Dynamik** (Zustandsautomat, Aktivitätsdiagramm, Petrinetz), **Logik** (Entscheidungstabelle, Entscheidungsbaum, Regeln).

## Karte 5
Die Klasse | Selbst bewerten
F: Wie lautet der Kerntest für die Entscheidung zwischen Klasse und Attribut?
A: **Objektidentität.** Könnte dieses Ding allein in der Welt stehen und hätte trotzdem Bedeutung? Dann Klasse. Sonst Attribut.

## Karte 6
Die Klasse
F: Was bedeuten die Zeichen `+`, `-`, `#` und `~` vor einem Attribut?
A: `+` public, `-` private, `#` protected, `~` package. Das ist die Notationsform des Geheimnisprinzips.

## Karte 7
Die Klasse
F: Wie werden abgeleitete Attribute und Klassenattribute notiert?
A: Abgeleitete Attribute mit vorangestelltem Schrägstrich (`/alter`), Klassenattribute unterstrichen.

## Karte 8
Die Klasse
F: Wie lautet die vollständige Attributsyntax?
A: `[Sichtbarkeit] name : Typ [Multiplizität] = Initialwert {Eigenschaftswerte}` — zum Beispiel `- datum: Date = aktuellesDatum {readOnly}`.

## Karte 9
Die Klasse
F: Was besagt der Isolationstest für Attribute?
A: Muss dieses Attribut auch dann zu jedem Objekt gehören, wenn man die Klasse völlig isoliert von allen anderen betrachtet? Wenn nein, gehört es vermutlich an eine Assoziation.

## Karte 10
Beziehungen zwischen Klassen | Selbst bewerten
F: Nenne die drei Kompositionskriterien.
A: 1. Es liegt eine "ist Teil von"-Beziehung vor. 2. Die Multiplizität am Ganzen beträgt höchstens 1. 3. Die Lebensdauer der Teile ist an die des Ganzen gebunden.

## Karte 11
Beziehungen zwischen Klassen
F: Weiße oder schwarze Raute — welche gehört wohin, und an welchem Ende steht sie?
A: **Weiß** = Aggregation, **schwarz** = Komposition. Die Raute steht immer **am Ganzen**.

## Karte 12
Beziehungen zwischen Klassen
F: Wann Enumeration, wann Vererbung?
A: Gleiche Attribute, nur andere Bezeichnung → Enumeration. Eigene Attribute pro Ausprägung → Vererbung.

## Karte 13
Beziehungen zwischen Klassen
F: Wann wird eine Oberklasse abstrakt, und wie wird sie notiert?
A: Wenn es kein Objekt gibt, das keiner ihrer Unterklassen angehört. Notation: Klassenname **kursiv**, alternativ `{abstract}`.

## Karte 14
Beziehungen zwischen Klassen
F: Was ist Balzerts Rat, wenn du dir bei einer Beziehungsart unsicher bist?
A: Im Zweifelsfall die **einfache Assoziation** verwenden. Die Aggregation kommt selten vor und ist unpräzise definiert.

## Karte 15
XML zum Klassendiagramm | Selbst bewerten
F: Nenne die sechs Übersetzungsregeln von XML nach UML.
A: 1. Mehrfach vorkommendes Element → Klasse. 2. Einfaches Kindelement oder XML-Attribut → Attribut. 3. Verschachtelung → Komposition. 4. Wiederholung → Multiplizität. 5. Sammelelement im Plural → gar nichts. 6. Verweis über ID → Assoziation.

## Karte 16
XML zum Klassendiagramm
F: Wie lautet der Merksatz zur Unterscheidung von Komposition und Assoziation in XML?
A: **Physische Verschachtelung ist Komposition. Verweis ist Assoziation.**

## Karte 17
XML zum Klassendiagramm
F: Was sind die zwei teuersten Fehler bei XML-Aufgaben?
A: 1. Ein Sammelelement als Klasse modellieren (kostet doppelt: überflüssige Klasse plus verlorene Multiplizität). 2. Einen Verweis als String-Attribut statt als Assoziation modellieren.

## Karte 18
Zustandsautomaten | Selbst bewerten
F: Wie ist eine Transitionsbeschriftung aufgebaut?
A: `Ereignis [Wächter] / Aktion` — alle drei Bestandteile sind optional. Eine Transition ohne Beschriftung ist ein implizites Ereignis.

## Karte 19
Zustandsautomaten
F: Was bedeuten entry, do und exit?
A: `entry` beim Betreten, `do` als Aktivität während des Verweilens, `exit` beim Verlassen — unabhängig davon, über welche Transition.

## Karte 20
Zustandsautomaten
F: Wie modellierst du "der Anwender kann jederzeit abbrechen"?
A: Als **zusammengesetzten Zustand** mit einem **Gruppenübergang** von seiner Grenze zum Endzustand. Aus vielen Pfeilen wird einer.

## Karte 21
Aktivitätsdiagramme und Petrinetze | Selbst bewerten
F: Raute oder Balken — was bedeutet was?
A: **Raute = Entweder-oder** (ein Weg wird gewählt). **Balken = Sowohl-als-auch** (Fork/Join, alle Wege parallel; der Join wartet auf alle Stränge).

## Karte 22
Aktivitätsdiagramme und Petrinetze
F: Wozu dienen Petrinetze, wenn es doch Aktivitätsdiagramme gibt?
A: Sie sind mathematisch fundiert. Auf Basis der Graphentheorie lässt sich formal beweisen, dass ein Ablauf nicht in einen Deadlock mündet.

## Karte 23
Entscheidungstabellen und Logik | Selbst bewerten
F: Wie viele Regeln hat eine formal vollständige Entscheidungstabelle, und aus welchen Quadranten besteht sie?
A: 2 hoch n Regeln bei n Bedingungen. Quadranten: Bedingungen, Bedingungsanzeiger (J/N/–), Aktionen, Aktionsanzeiger (X).

## Karte 24
Entscheidungstabellen und Logik
F: Wie funktioniert die Konsolidierung einer Entscheidungstabelle?
A: Regeln mit identischen Aktionen paarweise vergleichen. Unterscheiden sie sich nur in einer Bedingungszeile, zusammenfassen und den abweichenden Anzeiger durch einen Irrelevanzanzeiger (–) ersetzen.

## Karte 25
Requirements Engineering | Selbst bewerten
F: Welche vier Vertragsarten gibt es, und welche brauchen eine Leistungsbeschreibung?
A: Time and Material, Festpreis, Wartung, Service. **Festpreis und Wartung** brauchen eine Leistungsbeschreibung — bei der Wartung, weil ein Fehler eine Abweichung vom Soll ist.

## Karte 26
Requirements Engineering
F: Wie unterscheiden sich funktionale Anforderungen, nicht-funktionale Anforderungen und Randbedingungen?
A: **Funktional** = Features, was das System können muss. **Nicht-funktional** = Qualitätsattribute, querschneidend (Antwortzeit, Usability). **Randbedingung** = Restriktion (Termin, vorgeschriebene Datenbank, Betriebsbedingungen).

## Karte 27
Requirements Engineering
F: Was besagt das Kano-Modell?
A: **Basismerkmale** sind unterbewusst und selbstverständlich. **Leistungsmerkmale** werden bewusst gefordert. **Begeisterungsmerkmale** sind unbewusst — sie begeistern, werden aber nicht vermisst.

## Karte 28
Requirements Engineering
F: Was heißt es, eine nicht-funktionale Anforderung zu operationalisieren?
A: Sie in konkrete, prüfbare Anforderungen herunterbrechen. Aus "gute Usability" werden Kontrastwerte für Sehschwäche und einfache Sprache für Textverständlichkeit.

## Karte 29
Scrum und Prozessmodelle | Selbst bewerten
F: Wer priorisiert, wer schätzt in Scrum?
A: Der **Product Owner priorisiert** die Reihenfolge. Das **Team schätzt** — und zwar allein. Der ScrumMaster tut weder das eine noch das andere.

## Karte 30
Scrum und Prozessmodelle
F: Review oder Retrospektive — worin liegt der Unterschied?
A: **Review** schaut auf das **Produkt** und ist öffentlich (mit Stakeholdern). **Retrospektive** schaut auf den **Prozess** und ist teamintern.

## Karte 31
Scrum und Prozessmodelle
F: Warum eignet sich Scrum nicht für Festpreisprojekte?
A: Weil das Backlog ständig verändert wird, steht der Liefergegenstand erst im Laufe des Projekts fest. Ohne definierten Liefergegenstand keine Lieferverpflichtung — also Budget oder Time and Material.

## Karte 32
Scrum und Prozessmodelle
F: Was sind die vier Cynefin-Bereiche und ihre Handlungsfolgen?
A: **Offensichtlich**: erkennen, beurteilen, reagieren. **Kompliziert**: erkennen, analysieren, reagieren. **Komplex**: probieren, erkennen, reagieren. **Chaotisch**: handeln, erkennen, reagieren.

## Karte 33
Konfigurationsmanagement mit Git | Selbst bewerten
F: Welche vier Orte kennt Git, und welcher Befehl führt jeweils dorthin?
A: Working Directory → `add` → Staging Area → `commit` → Local Repository → `push` → Remote Repository.

## Karte 34
Konfigurationsmanagement mit Git
F: Welche fünf Zweigtypen kennt der Git-Flow, und wo darf entwickelt werden?
A: Master, Develop, Feature, Release, Hotfix. Entwickelt wird **nur in Feature-Branches**; in Release und Hotfix ausschließlich Bugfixes.

## Karte 35
Konfigurationsmanagement mit Git
F: Fast-Forward oder Three-Way — wann tritt was auf?
A: **Fast-Forward**, wenn sich am Ursprungszweig seit der Abzweigung nichts geändert hat. **Three-Way** im Regelfall, mit zusätzlichem Merge-Commit. Beide erhalten die Historie; Rebase schreibt sie um.

## Karte 36
Testgetriebene Entwicklung | Selbst bewerten
F: Wie lauten die drei Gesetze des TDD?
A: 1. Kein Code, außer um einen fehlgeschlagenen Test zu fixen. 2. Nicht mehr Testcode als nötig, um einen Fehlschlag zu erzeugen (Kompilierfehler zählen). 3. Nicht mehr Produktionscode als nötig, um den Test zu fixen.

## Karte 37
Testgetriebene Entwicklung
F: Was bedeuten Faking und Triangulation?
A: **Faking**: bewusst zu einfache Implementierung, um den Testaufbau selbst zu prüfen. **Triangulation**: weitere Testfälle hinzufügen, bis der Schritt zur Generalisierung gelingt.

## Karte 38
Testgetriebene Entwicklung
F: Wofür steht SOLID?
A: **S**ingle Responsibility, **O**pen-Closed, **L**iskovsches Substitutionsprinzip, **I**nterface Segregation, **D**ependency Inversion.

## Karte 39
Testgetriebene Entwicklung
F: Welche vier Metriken zur Codequalität nennen die Folien?
A: M1 McCabe (zyklomatische Komplexität), M2 Kopplung, M3 Kohäsion, M4 Code Smells. Ziel: schwache Kopplung, starke Kohäsion.

## Karte 40
Selbst bewerten | Klausurstrategie
F: Welche drei Fehler kosten in der Klausur die meisten Punkte?
A: 1. Fehlende Multiplizitäten an Assoziationsenden. 2. Container-Klassen bzw. Sammelelemente als Klasse. 3. Rollen als eigene Klassen modelliert.

# Nachschlag
## Prinzipien und Systembegriff
Die Grundvokabeln aus Balzert Kapitel 4.

- **Prinzip** — Grundsatz, den man seinem Handeln zugrunde legt; allgemeingültig, abstrakt, aus Erfahrung hergeleitet.
- **System** — Ausschnitt aus der realen oder gedanklichen Welt aus Systemkomponenten bzw. Subsystemen, die untereinander in Beziehungen stehen.
- **Systemelement** — Teil eines Systems, das nicht weiter zerlegt werden soll.
- **Abstraktion** — das Wesentliche aus dem Zufälligen herausheben, Unwesentliches weglassen. Gegenteil: Konkretisierung.
- **Strukturierung** — einem System ein Ordnungsgefüge geben; statisch, dynamisch oder organisatorisch.
- **Hierarchisierung** — Strukturierung mit Rangordnung (Vererbung, Pakete, XML-Bäume).
- **Modularisierung** — Zerlegung in Teile mit definierten Schnittstellen.
- **Geheimnisprinzip** — nach außen ist nur sichtbar, was sichtbar sein muss.
- **Kopplung** — Abhängigkeit zwischen Komponenten; soll **minimiert** werden.
- **Bindung / Kohäsion** — Zusammengehörigkeit innerhalb einer Komponente; soll **maximiert** werden.
- **Verbalisierung** — prägnante, fachlich passende Namen; bei der Namensgebung zeigt sich, ob die Struktur stimmt.

## Modellbegriff
Was ein Modell ist und welche Arten unterschieden werden.

- **Modell** — Abstraktion der Wirklichkeit.
- **Abbildung / Verkürzung / Pragmatik** — die drei Eigenschaften jedes Modells.
- **Deskriptives Modell** — beschreibt eine bestehende Wirklichkeit.
- **Präskriptives Modell** — Vorbild für ein noch nicht existierendes System.
- **Typ-Ebene** — Ebene der Vorlagen; hier lebt das Klassendiagramm.
- **Exemplar-Ebene** — Ebene konkreter Objekte mit Werten; hier lebt das Objektdiagramm.
- **Meta-Ebene** — die Regeln der Notation selbst, also die UML-Spezifikation.
- **Basiskonzept** — atomares, konzeptionell langlebiges, vielseitig einsetzbares Konzept.
- **Notation** — Darstellung von Informationen durch Symbole: textuell, grafisch oder formal.

## Statik — Klassendiagramm
Vokabeln rund um Klassen, Attribute und Beziehungen.

- **Klasse** — Beschreibung gleichartiger Objekte auf der Typ-Ebene; Rechteck mit bis zu drei Fächern.
- **Objekt** — Exemplar einer Klasse; notiert als `objektname : Klassenname`, unterstrichen.
- **Attribut** — Eigenschaft einer Klasse; Syntax `[Sicht] name : Typ [Mult] = Init {Props}`.
- **Klassenattribut** — Attribut mit gleichem Wert für alle Objekte; **unterstrichen**.
- **Abgeleitetes Attribut** — wird berechnet, nicht gespeichert; Schrägstrich vor dem Namen.
- **Enumeration** — Datentyp mit fester, endlicher Wertemenge; Stereotyp `«enumeration»`.
- **Strukturierter Datentyp** — Bündel von Werten ohne eigene Identität; Stereotyp `«datatype»`.
- **Assoziation** — Beziehung zwischen **gleichrangigen** Klassen.
- **Multiplizität** — Anzahl beteiligter Objekte je Beziehungsende: `1`, `0..1`, `*`, `1..*`.
- **Rollenname** — Substantiv am Assoziationsende; beschreibt die Rolle in dieser Beziehung.
- **Assoziationsklasse** — trägt Attribute, die nur für die Kombination zweier Objekte gelten.
- **Generalisierung / Vererbung** — Dreieck zur Oberklasse; vererbt Attribute, Operationen **und** Assoziationen.
- **Abstrakte Klasse** — nicht instanziierbar; Klassenname **kursiv**.
- **Aggregation** — Ganzes-Teil-Beziehung, Teil kann zu mehreren Ganzen gehören; **weiße** Raute am Ganzen.
- **Komposition** — starke Ganzes-Teil-Beziehung, Teil lebt und stirbt mit dem Ganzen; **schwarze** Raute am Ganzen.

## Dynamik — Zustand und Ablauf
Vokabeln der Verhaltensmodellierung.

- **Zustand** — Situation, in der das System verweilt; Name als Adjektiv oder Partizip, nie als Verb.
- **Transition** — Zustandsübergang; beschriftet mit `Ereignis [Wächter] / Aktion`.
- **Wächter (guard)** — zusätzliche Bedingung in eckigen Klammern, die beim Ereignis wahr sein muss.
- **Aktion** — braucht im Idealfall keine Zeit, wird immer vollständig ausgeführt.
- **Aktivität** — braucht Zeit, kann durch Ereignisse vorzeitig beendet werden; als `do` im Zustand.
- **Implizites Ereignis** — Transition ohne Beschriftung; feuert, wenn die Verarbeitung im Zustand endet.
- **Gruppenübergang** — Transition von der Grenze eines zusammengesetzten Zustands aus.
- **Historie** — `H` merkt sich den zuletzt aktiven Unterzustand, `H*` über alle Verfeinerungsstufen.
- **Mealy / Moore / Harel** — Ausgabe am Übergang / am Zustand / beides kombiniert (die UML-Variante).
- **Fork und Join** — dicker Balken; Fork teilt in parallele Stränge, Join **wartet** auf alle.
- **Aktivitätsbereich (Swimlane)** — ordnet Aktionen den ausführenden Akteuren zu.
- **Petrinetz** — Stellen, Transitionen und Marken; formal analysierbar, u. a. auf Deadlock-Freiheit.
- **Schaltregel** — eine Transition schaltet, wenn alle Eingangsstellen mindestens eine Marke tragen.

## Logik — Entscheidungstabellen
Vokabeln aus Balzert Kapitel 11.

- **Entscheidungstabelle** — vier Quadranten: Bedingungen, Bedingungsanzeiger, Aktionen, Aktionsanzeiger.
- **Regel** — eine Spalte der Tabelle; bei n Bedingungen gibt es 2^n davon.
- **Bedingungsanzeiger** — `J`, `N` oder `–` (Irrelevanzanzeiger).
- **Formal vollständig** — alle 2^n Kombinationen eingetragen.
- **Inhaltlich vollständig** — alle praktisch möglichen Kombinationen eingetragen.
- **Konsolidierung** — Zusammenfassen von Regeln, die sich bei gleichen Aktionen nur in einer Zeile unterscheiden.
- **Else-Regel** — fängt alle nicht abgedeckten Fälle auf; ohne Bedingungsanzeiger, nur eine pro Tabelle.
- **Eintreffer- / Mehrtreffer-Tabelle** — genau eine anwendbare Regel / mehrere gleichzeitig anwendbare Regeln.
- **Auswertungsvektor** — die konkrete Belegung der Bedingungen zur Laufzeit.
- **Konfliktmenge** — Menge der Regeln, deren Bedingungsteil erfüllt ist.

## Requirements Engineering
Vokabeln aus Balzert Teil IV.

- **Lastenheft** — Auftraggebersicht: was gefordert wird. Kürzel `/LV/ /LZ/ /LR/ /LK/ /LF/ /LQ/`.
- **Pflichtenheft** — Auftragnehmersicht: was geliefert wird; Verfeinerung des Lastenhefts.
- **Stakeholder** — Person mit einem Belang am System; aus Belangen entstehen Anforderungen (IEEE 1471).
- **Funktionale Anforderung** — Feature, das das System bieten muss.
- **Nicht-funktionale Anforderung** — Qualitätsattribut, querschneidend (Antwortzeit, Usability, Sicherheit).
- **Randbedingung / Restriktion** — organisatorisch (Zielgruppe, Betriebszeit) oder technisch (Hardware, Software).
- **Operationalisieren** — eine nicht-funktionale Anforderung in konkrete, prüfbare Anforderungen herunterbrechen.
- **Kano-Modell** — Basismerkmale (unterbewusst), Leistungsmerkmale (bewusst), Begeisterungsmerkmale (unbewusst).
- **Modalverben** — `muss` (Pflicht), `sollte` (Wunsch), `wird` (Absichtserklärung).
- **Analogiemethode** — Schätzung durch Vergleich mit einem ähnlichen abgeschlossenen Projekt.
- **Prozentsatzmethode** — Hochrechnung vom bekannten Aufwand einer Phase auf das Gesamtvolumen.
- **Wideband-Delphi** — Expertenschätzung in mehreren anonymen Runden mit Rückmeldung.
- **Function Points** — Messung des funktionalen Umfangs aus Benutzersicht (ISO/IEC 20926).
- **COCOMO II** — algorithmisches Schätzmodell mit drei Stufen je nach Projektzeitpunkt.
- **Gewährleistung vs. Wartung** — gesetzlicher Anspruch nach Lieferung vs. vertraglich vereinbarte Pflege (10–25 % p. a.).

## Scrum
Vokabeln aus dem Scrum-Buch und LE 7.

- **Empirischer Prozess** — beobachten und nachsteuern statt langfristig planen.
- **Transparenz, Inspektion, Adaption** — die drei Säulen von Scrum.
- **Product Owner** — der Visionär; priorisiert und verantwortet den Wert.
- **Entwicklungsteam** — die Lieferanten; selbstorganisiert, schätzt, verantwortet die Qualität.
- **ScrumMaster** — der Change Agent; löst Hindernisse, **nicht weisungsbefugt**.
- **Product Backlog** — priorisierte Liste aller Anforderungen; veränderlich.
- **Sprint Backlog** — Auswahl für den aktuellen Sprint.
- **Increment** — potenziell auslieferbares Produktinkrement am Sprintende.
- **Sprint Review** — öffentlich, schaut auf das **Produkt**.
- **Retrospektive** — teamintern, schaut auf den **Prozess**.
- **Definition of Done** — Vereinbarung, wann ein Backlog Item wirklich fertig ist.
- **Story Points / Velocity** — relative Schätzgröße / geschaffte Punkte pro Sprint.
- **Impediment** — Hindernis, das der ScrumMaster aus dem Weg räumt.
- **Cynefin** — Ordnungsrahmen: offensichtlich, kompliziert, komplex, chaotisch.

## Konfigurationsmanagement
Vokabeln aus LE 2 und LE 7.

- **Konfiguration** — konsistenter Stand aller Artefakte eines Systems zu einem Zeitpunkt.
- **Version** — Gesamtmenge aller Dateien und ihrer Stände, nicht der Stand einer Einzeldatei.
- **Snapshot** — Git speichert Zustände des gesamten Projekts, keine Deltas pro Datei.
- **Working Directory** — die Arbeitskopie auf dem Rechner.
- **Staging Area** — Vormerkliste für den nächsten Commit.
- **Local Repository** — lokaler Verlauf; Commits hier sind für andere **unsichtbar**.
- **Remote Repository** — der geteilte Stand auf dem Server; erreichbar erst nach `push`.
- **Branch** — paralleler Entwicklungszweig.
- **Git-Flow** — Master, Develop, Feature, Release, Hotfix.
- **Fast-Forward-Merge** — Commits werden angehängt, weil sich der Ursprung nicht geändert hat.
- **Three-Way-Merge** — echtes Zusammenführen zweier auseinandergelaufener Stände; erzeugt einen Merge-Commit.
- **Rebase** — schreibt die Historie um (im Gegensatz zum Merge).
- **Continuous Integration** — Commit, Build, Test, Paketierung, Deployment mit Feedback in jeder Stufe.

## Testgetriebene Entwicklung
Vokabeln aus LE 8.

- **Test Driven Design** — Anforderungen in Tests überführen und die Logik entlang dieser Tests entwickeln.
- **Red, Green, Refactor** — der TDD-Workflow. Motto: Make it green, then make it clean.
- **Faking** — bewusst zu einfache Implementierung, um den Testaufbau selbst zu prüfen.
- **Triangulation** — weitere Testfälle hinzufügen, bis die Generalisierung gelingt.
- **Refactoring** — Strukturverbesserung ohne Verhaltensänderung, bei grünen Tests.
- **Software-Entropie** — die Tendenz von Software zur Unordnung über die Zeit.
- **McCabe-Metrik** — zyklomatische Komplexität; Anzahl unabhängiger Pfade.
- **Kopplung / Kohäsion** — Ziel: Kopplung schwach, Kohäsion stark.
- **SOLID** — Single Responsibility, Open-Closed, Liskov, Interface Segregation, Dependency Inversion.
- **Code Smell** — strukturelles Warnzeichen im Quellcode.

## Klausurstrategie
Signalwörter im Aufgabentext und die häufigsten Fehler.

**Signalwörter**

- "ergibt sich aus", "die Summe aller" → **abgeleitetes Attribut** `/name`
- "kann die Werte X, Y, Z annehmen" → **Enumeration**
- "es gibt drei Arten von …" + eigene Attribute → **Vererbung**, Oberklasse ggf. abstrakt
- "ist eine besondere Form von …" → Vererbung **auf der genannten Stufe**
- "besteht aus", "enthält", explizites Löschverhalten → **Komposition**
- "alle Versuche werden gespeichert" → **Historie**, Multiplizität `*`
- "eindeutig" → `{id}` oder `{unique}`
- "jederzeit kann abgebrochen werden" → zusammengesetzter Zustand mit **Gruppenübergang**
- "sobald abgeschlossen" → **implizites Ereignis**
- Sammelelement im Plural (XML) → **keine Klasse**
- Verweis über ID (XML) → **Assoziation**

**Die häufigsten Fehler**

1. Fehlende Multiplizitäten an einem Assoziationsende
2. Container-Klassen bzw. Sammelelemente als Klasse modelliert
3. Rollen als eigene Klassen statt an der Assoziation
4. Enumeration und Vererbung verwechselt
5. XML-Attribute in der Anfangsmarkierung übersehen
6. Zu früh gezeichnet statt erst Klassen- und Attributliste erstellt
