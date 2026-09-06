# Fach: Machine Learning Klausurvorbereitung

# Test
## Grundlagen & Lernparadigmen
Lernarten, Mitchell-Definition, Overfitting, Train/Val/Test

### Aufgabe
Typ: radio
F: Was unterscheidet überwachtes von unüberwachtem Lernen laut Kursdefinition am zentralsten?
O: Die Menge der verfügbaren Rechenleistung
O: *Ob Trainingsdaten Labels (Lösungen) enthalten
O: Die Anzahl der verwendeten Merkmale
O: Ob ein neuronales Netz verwendet wird
A: Überwacht = Daten enthalten Labels; unüberwacht = keine Labels vorhanden.

### Aufgabe
Typ: checkbox
F: Welche der folgenden Verfahren gehören zum unüberwachten Lernen?
O: *k-Means
O: *DBSCAN
O: *PCA
O: Logistische Regression
O: Random Forest
A: k-Means und DBSCAN sind Clustering, PCA ist Dimensionsreduktion — alle drei unüberwacht. Logistische Regression und Random Forest sind überwacht.

### Aufgabe
Typ: checkbox
F: Welche vier Aufgabenfamilien gehören zum unüberwachten Lernen?
O: *Clustering
O: *Anomalie-/Neuheitserkennung
O: *Dimensionsreduktion/Visualisierung
O: *Assoziationsregeln
O: Klassifikation
A: Klassifikation ist eine überwachte Aufgabe. Die vier genannten sind die unüberwachten Aufgabenfamilien.

### Aufgabe
Typ: truefalse
F: Bei halbüberwachtem Lernen ist der komplette Datensatz gelabelt.
L: false
A: Halbüberwacht heißt: nur ein kleiner Teil der Daten ist gelabelt.

### Aufgabe
Typ: radio
F: Wie erzeugt selbstüberwachtes Lernen (Self-Supervised) seine Labels?
O: Durch menschliche Annotation
O: *Aus den Daten selbst, z. B. durch Masking
O: Durch ein Belohnungssignal
O: Durch Clustering ähnlicher Instanzen
A: Self-Supervised erzeugt Labels aus den Daten selbst, z. B. durch Verdecken und Rekonstruieren eines Bildausschnitts.

### Aufgabe
Typ: radio
F: Was benutzt Reinforcement Learning anstelle von Labels?
O: Clusterzentren
O: Eine Kostenfunktion
O: *Ein Belohnungssignal
O: Eine Konfusionsmatrix
A: Reinforcement Learning arbeitet mit Belohnung/Strafe statt Labels; ein Agent optimiert seine Policy.

### Aufgabe
Typ: fillblank
F: Es gilt die Mengen-Hierarchie: {{Deep Learning;DL}} ⊂ {{Machine Learning;ML}} ⊂ {{Künstliche Intelligenz;KI}}.
A: DL ist Teilmenge von ML, ML ist Teilmenge von KI. Data Science überlappt nur, ist keine Teil-/Obermenge.

### Aufgabe
Typ: radio
F: Ab wie vielen Schichten spricht man laut Kursdefinition von Deep Learning?
O: Ab 1 Schicht
O: Ab 2 Schichten
O: *Ab 3 Schichten
O: Ab 10 Schichten
A: Deep Learning = neuronales Netz mit mindestens 3 Layern.

### Aufgabe
Typ: truefalse
F: Data Science ist eine echte Teilmenge von Machine Learning.
L: false
A: Data Science überlappt mit ML/KI, ist aber weder Teil- noch Obermenge.

### Aufgabe
Typ: fillblank
F: In der Mitchell-Definition lernt ein Programm aus Erfahrung {{E}} bezüglich einer Aufgabe {{T}} und einem Leistungsmaß {{P}}, wenn P mit E steigt.
A: Klassische ML-Definition von Tom Mitchell (1997).

### Aufgabe
Typ: block
F: Ordnen Sie beim Spamfilter-Beispiel die Mitchell-Buchstaben ihrer Bedeutung zu.
S: T (Task)
S: E (Experience)
S: P (Performance)
K: Neue Mails als Spam kennzeichnen -> T (Task)
K: Gelabelte Trainingsmails -> E (Experience)
K: Anteil korrekt klassifizierter Mails -> P (Performance)
A: T = Aufgabe, E = Erfahrung (Trainingsdaten), P = Leistungsmaß (z. B. Accuracy).

### Aufgabe
Typ: radio
F: Welche Definition stammt von Arthur Samuel (1959)?
O: Ein Computerprogramm lernt aus Erfahrung E bzgl. T und P
O: *ML gibt Computern die Fähigkeit zu lernen, ohne explizit programmiert zu werden
O: DL ist ein NN mit mindestens 3 Layern
O: Overfitting ist das Auswendiglernen von Trainingsdaten
A: Die erste Definition stammt von Mitchell (1997), diese informelle von Samuel (1959).

### Aufgabe
Typ: radio
F: Ein Modell soll einen kontinuierlichen Hauspreis vorhersagen. Um welche Aufgabe handelt es sich?
O: Klassifikation
O: *Regression
O: Clustering
O: Assoziationsanalyse
A: Kontinuierliche Zielgröße = Regression.

### Aufgabe
Typ: truefalse
F: Die logistische Regression ist trotz ihres Namens ein Klassifikationsverfahren.
L: true
A: Sie liefert eine Zugehörigkeitswahrscheinlichkeit und wird für Klassifikation eingesetzt.

### Aufgabe
Typ: radio
F: Was passiert bei Batch-Learning (im Sinne von Offline-Learning), wenn neue Daten hinzukommen?
O: Das Modell lernt die neuen Daten inkrementell dazu
O: *Es muss komplett neu trainiert werden (alte + neue Daten)
O: Nur die neuen Daten werden verwendet
O: Das Modell verwirft die neuen Daten automatisch
A: Batch-Learning erfordert bei neuen Daten ein komplettes Neu-Training mit dem Gesamtdatensatz.

### Aufgabe
Typ: checkbox
F: Welche Aussagen zu Online-Learning treffen zu?
O: *Es eignet sich für Datenströme mit begrenzten Ressourcen
O: *Verarbeitete Daten können verworfen werden
O: Es ist identisch mit Batch-Learning
O: Es kann niemals "abdriften"
A: Online-Learning verarbeitet Daten inkrementell und ist ressourcenschonend, kann aber bei schlechten Daten "abdriften".

### Aufgabe
Typ: radio
F: Was ist mit "Batch" im Kontext des Gradientenverfahrens (2. Bedeutung) gemeint?
O: Offline-Training mit allen Daten
O: *Ein Datenhäppchen pro GD-Schritt
O: Der komplette Testdatensatz
O: Eine komplette Epoche
A: Diese zweite Bedeutung von "Batch" ist die Häppchengröße pro Gradientenschritt, nicht das Offline-Learning-Konzept.

### Aufgabe
Typ: fillblank
F: Eine {{Epoche}} entspricht einem vollständigen Durchlauf durch den gesamten Trainingsdatensatz.
A: Grundbegriff des iterativen Trainings.

### Aufgabe
Typ: truefalse
F: Out-of-Core-Lernen läuft trotz des Namens "Online-Learning-ähnlich" in der Regel offline ab.
L: true
A: Out-of-Core lädt Daten häppchenweise, weil sie nicht in den Speicher passen, das Training selbst ist aber i. d. R. offline (inkrementelles Lernen).

### Aufgabe
Typ: radio
F: Was ist der Kern des instanzbasierten Lernens (z. B. k-NN)?
O: Eine Funktion wird explizit gelernt und eine Kostenfunktion minimiert
O: *Beispiele werden gespeichert, neue Punkte per Ähnlichkeitsmaß verglichen
O: Es wird immer ein neuronales Netz verwendet
O: Es gibt keine Trainingsphase
A: Instanzbasiert = "auswendig lernen" + Ähnlichkeitsmaß, kein explizites Modell.

### Aufgabe
Typ: radio
F: Was bedeutet "Hyperebene"?
O: Eine ausschließlich gebogene Trennfläche
O: *Eine Trennfläche der Dimension (n−1) im n-dimensionalen Raum
O: Ein Modell mit besonders vielen Hyperparametern
O: Eine Ebene nur in 3D-Räumen
A: Hyperebene verallgemeinert die Trennlinie/-ebene auf beliebige Dimensionen; gerade = linear, gebogen = nichtlinear.

### Aufgabe
Typ: checkbox
F: Welche der folgenden sind Hyperparameter (nicht Modellparameter)?
O: *Lernrate
O: *k bei k-NN
O: *Regularisierungsstärke α
O: Die gelernten Gewichte θ
A: Hyperparameter werden vor dem Training gesetzt; θ (Gewichte) werden vom Algorithmus gelernt.

### Aufgabe
Typ: radio
F: Was zeigt Overfitting typischerweise in den Loss-Kurven?
O: Beide Kurven bleiben konstant hoch
O: Trainingsloss steigt, Validierungsloss sinkt
O: *Trainingsloss sinkt weiter, Validierungsloss steigt wieder (Divergenz)
O: Beide Kurven sinken exakt gleich
A: Divergenz der Kurven (Val-Loss steigt trotz sinkendem Train-Loss) ist das Overfitting-Signal.

### Aufgabe
Typ: checkbox
F: Welche Maßnahmen helfen gegen Overfitting?
O: *Mehr Trainingsdaten
O: *Regularisierung
O: *Einfacheres Modell
O: Ein mächtigeres Modell mit mehr Parametern
A: Ein mächtigeres Modell hilft gegen Underfitting, nicht gegen Overfitting — das ist die klassische Verwechslungsfalle.

### Aufgabe
Typ: checkbox
F: Welche Maßnahmen helfen gegen Underfitting?
O: *Mächtigeres Modell
O: *Besseres Feature Engineering
O: *Regularisierung verringern
O: Mehr Trainingsdaten sammeln
A: Mehr Daten helfen nur gegen Overfitting, nicht gegen Underfitting.

### Aufgabe
Typ: radio
F: Worin unterscheiden sich Sampling Bias und Stichprobenrauschen?
O: Es gibt keinen Unterschied
O: *Sampling Bias entsteht durch fehlerhafte Erhebungsmethode (auch bei großen Stichproben), Stichprobenrauschen durch zu kleine Stichprobe (Zufall)
O: Stichprobenrauschen tritt nur bei k-NN auf
O: Sampling Bias ist nur bei Regression relevant
A: Sampling Bias ist ein methodischer Fehler; Stichprobenrauschen ist reiner Zufall bei kleinen Stichproben.

### Aufgabe
Typ: radio
F: Warum dürfen sich Trainings- und Testdaten niemals überschneiden?
O: Aus rechtlichen Gründen
O: *Sonst wird die Fehlerschätzung zu optimistisch (Data Leakage)
O: Weil sklearn das technisch verbietet
O: Weil dann keine Kreuzvalidierung möglich ist
A: Überschneidung führt zu Data Leakage und einer zu optimistischen Generalisierungsschätzung.

### Aufgabe
Typ: truefalse
F: Hyperparameter dürfen auf dem Testset getunt werden, solange man es nur einmal tut.
L: false
A: Hyperparameter werden ausschließlich auf dem Validierungsset getunt; das Testset dient nur der finalen, einmaligen Bewertung.

### Aufgabe
Typ: radio
F: Was bedeutet Stratifizierung beim Train-Test-Split?
O: Zufällige Sortierung der Daten
O: *Beibehaltung des Klassenverhältnisses in allen Teilmengen
O: Verwendung von k-facher Kreuzvalidierung
O: Entfernen von Ausreißern
A: Stratifizieren = gleiche Klassenverteilung in Train/Test/Val sicherstellen.

### Aufgabe
Typ: truefalse
F: Bei Zeitreihendaten darf man vor dem Split beliebig shuffeln.
L: false
A: Zeitreihen dürfen nicht geshuffelt werden, da das die zeitliche Struktur zerstört.

### Aufgabe
Typ: radio
F: Was wird bei k-facher Kreuzvalidierung am Ende reportet?
O: Nur der beste Fold
O: *Mittelwert der Performances plus Streuung
O: Nur der schlechteste Fold
O: Die Trainingszeit
A: Man reportet Mittelwert ± Standardabweichung über alle Folds.

### Aufgabe
Typ: radio
F: Warum sind neuronale Netze Black-Box-Modelle?
O: Weil sie langsam trainieren
O: *Weil man nur die Performance misst, aber nicht direkt sieht, warum eine Entscheidung fällt
O: Weil sie nur für Bilddaten geeignet sind
O: Weil sie keine Hyperparameter haben
A: Black Box = Entscheidungsfindung nicht nachvollziehbar, im Gegensatz zu White-Box-Modellen wie Entscheidungsbäumen.

### Aufgabe
Typ: fillblank
F: Das {{No-Free-Lunch}}-Theorem besagt: Ohne Annahmen über die Daten ist kein Modell a priori besser als ein anderes.
A: Wolpert (1996) — in der Praxis trifft man sinnvolle Annahmen und testet wenige plausible Modelle.

### Aufgabe
Typ: block
F: Ordnen Sie die Dozenten-Heuristik den passenden Modelltypen zu.
S: Bilddaten
S: Textdaten
S: Kleine Datenmengen (~200 Punkte)
K: CNN -> Bilddaten
K: RNN -> Textdaten
K: Random Forest -> Kleine Datenmengen (~200 Punkte)
A: Faustregeln aus dem No-Free-Lunch-Kontext.

### Aufgabe
Typ: radio
F: Was ist ein Beispiel für ein Datenproblem "irrelevante Merkmale"?
O: Zu wenige Trainingsdaten
O: Fehlerhafte Erhebungsmethode
O: *Ein Merkmal ohne Task-Bezug oder ohne Zusatzinformation
O: Label-Rauschen durch subjektive Bewertung
A: Irrelevante Merkmale liefern keinen Mehrwert zur Aufgabe — "Müll rein, Müll raus".

## ML-Workflow, Datenvorbereitung & Fehlermaße
Estimator/Transformer/Predictor, Pipelines, Skalierung, Fehlermaße

### Aufgabe
Typ: radio
F: Welche Methode(n) hat ein reiner Estimator in sklearn?
O: *Nur fit()
O: fit() und transform()
O: fit() und predict()
O: transform() und predict()
A: Estimator = Basisklasse mit fit(). Transformer ergänzt transform(), Predictor ergänzt predict().

### Aufgabe
Typ: checkbox
F: Welche Aussagen zur Estimator/Transformer/Predictor-Hierarchie sind korrekt?
O: *Jeder Transformer ist ein Estimator
O: *Jeder Predictor ist ein Estimator
O: Jeder Estimator ist ein Predictor
O: fit_predict() existiert bei jedem Predictor
A: Transformer und Predictor sind spezialisierte Estimatoren; fit_predict() gibt es nur bei Clustering/Anomalieverfahren.

### Aufgabe
Typ: truefalse
F: LinearRegression besitzt eine fit_predict()-Methode.
L: false
A: fit_predict() existiert nur bei Verfahren wie KMeans, DBSCAN, IsolationForest.

### Aufgabe
Typ: radio
F: Woran erkennt man in sklearn ein gelerntes (trainiertes) Attribut?
O: Großbuchstaben im Namen
O: *Ein Unterstrich am Ende des Namens
O: Ein Unterstrich am Anfang des Namens
O: Es gibt keine Konvention
A: Gelernte Attribute enden auf _, z. B. statistics_, best_params_, feature_importances_.

### Aufgabe
Typ: radio
F: Worauf darf fit() bzw. fit_transform() aufgerufen werden?
O: Nur auf Testdaten
O: Auf Trainings- UND Testdaten gleichermaßen
O: *Ausschließlich auf Trainingsdaten
O: Nur auf dem gesamten, ungesplitteten Datensatz
A: fit lernt Parameter nur aus Trainingsdaten; Test/Produktion nutzen nur transform/predict.

### Aufgabe
Typ: truefalse
F: Ruft man fit_transform() auf den Testdaten auf, spricht man von Data Leakage.
L: true
A: Das schleust Testwissen ins Modell ein und macht die Fehlerschätzung zu optimistisch.

### Aufgabe
Typ: radio
F: Was tut der Pipeline-Transformer aus scikit-learn im Vergleich zur Deep-Learning-Architektur "Transformer"?
O: Beide sind identisch
O: *Es sind zwei völlig unterschiedliche Konzepte mit demselben Namen
O: Der Pipeline-Transformer basiert auf Attention
O: Der DL-Transformer ist ein sklearn-Objekt
A: Klassische Fangfrage — reine Namensgleichheit, kein inhaltlicher Zusammenhang.

### Aufgabe
Typ: radio
F: Was muss der letzte Schritt einer Pipeline sein, damit die gesamte Pipeline eine predict()-Methode hat?
O: Ein Imputer
O: Ein Scaler
O: *Ein Predictor
O: Ein OneHotEncoder
A: Hängt man einen Predictor als letzten Schritt an, erbt die ganze Pipeline predict().

### Aufgabe
Typ: fillblank
F: Bei GridSearchCV adressiert man Parameter einzelner Pipeline-Schritte mit doppeltem {{Unterstrich}}, z. B. schritt__param.
A: Notation für verschachtelte Hyperparameter in Pipelines.

### Aufgabe
Typ: radio
F: Wann verwendet man RandomizedSearchCV statt GridSearchCV?
O: Wenn nur ein einziger Hyperparameter getestet wird
O: *Bei großen/kontinuierlichen Suchräumen
O: Wenn kein Validierungsset existiert
O: Nie, GridSearchCV ist immer vorzuziehen
A: RandomizedSearch zieht n_iter zufällige Kombinationen — effizienter bei großen Räumen.

### Aufgabe
Typ: fillblank
F: Bei RandomizedSearchCV ist die Anzahl der Trainingsläufe gleich {{n_iter}} mal {{cv}}.
A: Beide Faktoren bestimmen die Gesamtzahl der Fits.

### Aufgabe
Typ: radio
F: Warum liefert scoring='neg_root_mean_squared_error' negative Werte?
O: Ein Programmierfehler in sklearn
O: *Scoring-Funktionen sind als Nutzen definiert (größer=besser), daher wird das Vorzeichen umgedreht
O: Weil der RMSE negativ sein kann
O: Weil GridSearchCV nur negative Werte akzeptiert
A: sklearn erwartet "höher = besser"; Fehlermaße werden deshalb negiert.

### Aufgabe
Typ: checkbox
F: Welche kategorialen Merkmale sollten mit OneHotEncoder statt OrdinalEncoder codiert werden?
O: *Nominale Merkmale ohne natürliche Reihenfolge (z. B. Ortsnamen)
O: Ordinale Merkmale mit klarer Reihenfolge (z. B. Schulnoten)
O: *Farben (rot, grün, blau)
O: Niemals irgendwelche Merkmale
A: OneHot passt zu nominalen Merkmalen; ordinale dürfen durchnummeriert werden (OrdinalEncoder).

### Aufgabe
Typ: radio
F: Was unterscheidet pd.get_dummies() vom sklearn OneHotEncoder?
O: get_dummies ist schneller
O: *get_dummies merkt sich keine Kategorien, OneHotEncoder speichert die gelernten categories_
O: OneHotEncoder funktioniert nur mit Zahlen
O: Es gibt keinen Unterschied
A: Für ML-Pipelines ist OneHotEncoder vorzuziehen, weil er neue/fehlende Kategorien bei neuen Daten konsistent behandelt.

### Aufgabe
Typ: radio
F: Warum ist Skalierung vor dem Gradientenverfahren wichtig?
O: Skalierung ist nur bei Bäumen wichtig
O: *Unterschiedliche Wertebereiche erzeugen längliche Ellipsen statt Kreise in der Fehlerfläche, was das Training verlangsamt
O: Ohne Skalierung divergiert das Verfahren immer
O: Skalierung ist nur für Klassifikation nötig
A: Skalierung macht die Fehlerfläche kreisförmiger, der Gradient läuft direkter zum Minimum.

### Aufgabe
Typ: checkbox
F: Welche Scaler-Eigenschaften sind korrekt?
O: *StandardScaler: kein fester Wertebereich, robuster gegen Ausreißer
O: *MinMaxScaler: fester Wertebereich, empfindlich gegen Ausreißer
O: StandardScaler skaliert immer auf [0,1]
O: MinMaxScaler ist robuster gegen Ausreißer als StandardScaler
A: StandardScaler standardisiert (z-Score), MinMaxScaler skaliert auf festen Bereich und ist ausreißerempfindlicher.

### Aufgabe
Typ: truefalse
F: Der Scaler wird sowohl auf Trainings- als auch auf Testdaten gefittet.
L: false
A: fit_transform nur auf Train, transform auf Test — Grundregel gegen Data Leakage.

### Aufgabe
Typ: radio
F: Was bedeutet Data Snooping Bias?
O: Ein Fehler beim Programmieren des Scalers
O: *Wissen über Testdaten fließt vor dem Split unbewusst in Modellentscheidungen ein
O: Zu viele Hyperparameter werden getestet
O: Der Testdatensatz ist zu klein
A: Deshalb wird das Testset sofort nach dem Laden abgetrennt, vor der Datenexploration.

### Aufgabe
Typ: radio
F: Welches Encoding wird häufig für CSV-Dateien mit deutschen Umlauten verwendet?
O: UTF-16
O: *ISO-8859-1 (Latin-1)
O: ASCII
O: Base64
A: Deutsche Umlaute in älteren CSVs erfordern oft explizit Latin-1-Encoding beim Einlesen.

### Aufgabe
Typ: truefalse
F: df2 = df erzeugt in Pandas eine unabhängige Kopie von df.
L: false
A: Das erzeugt nur eine Referenz; für eine echte Kopie braucht man df.copy(deep=True).

### Aufgabe
Typ: radio
F: Warum ist der Mean Error (ME) als Qualitätsmaß ungeeignet?
O: Er ist zu rechenintensiv
O: *Positive und negative Fehler löschen sich gegenseitig aus
O: Er kann nur bei Klassifikation verwendet werden
O: Er ist identisch mit dem MAE
A: ME täuscht einen kleinen Fehler vor, weil sich Vorzeichen aufheben können.

### Aufgabe
Typ: checkbox
F: Welche drei Gründe sprechen für MSE statt MAE als Trainings-Kostenfunktion?
O: *Das Quadrat löst das Vorzeichenproblem
O: *Große Abweichungen werden stärker bestraft
O: *Mathematisch einfacher (differenzierbar, ein Extrempunkt)
O: MSE ist immer kleiner als MAE
A: Die drei genannten Gründe sind die Standardargumente für MSE.

### Aufgabe
Typ: radio
F: Welches Fehlermaß entspricht in etwa der Manhattan-Norm (ℓ1) und ist robuster bei Ausreißern?
O: MSE
O: RMSE
O: *MAE
O: ME
A: MAE ≈ ℓ1-Norm, robuster gegenüber Ausreißern als RMSE (≈ ℓ2-Norm).

### Aufgabe
Typ: fillblank
F: Der Korrelationskoeffizient r liegt immer im Bereich {{[-1,1];-1 bis 1}}.
A: r ∈ [−1, 1], wobei nur der Betrag über die Stärke des (linearen) Zusammenhangs entscheidet.

### Aufgabe
Typ: truefalse
F: Der Korrelationskoeffizient kann auch starke nichtlineare Zusammenhänge zuverlässig erkennen.
L: false
A: r erfasst ausschließlich lineare Zusammenhänge; bei nichtlinearen Mustern kann r trotzdem nahe 0 liegen.

### Aufgabe
Typ: radio
F: Was bedeutet eine hohe Korrelation zwischen zwei Merkmalen?
O: Zwingend eine kausale Beziehung
O: *Einen starken linearen Zusammenhang, aber keine automatische Kausalität
O: Dass eines der Merkmale entfernt werden muss
O: Dass beide Merkmale identisch sind
A: Korrelation ≠ Kausalität — Klassiker.

### Aufgabe
Typ: block
F: Ordnen Sie jedem ML-Projektschritt seine richtige Position in der 7-Schritte-Reihenfolge zu (grob).
S: Früh im Projekt
S: Mitte des Projekts
S: Spät im Projekt
K: Gesamtbild betrachten -> Früh im Projekt
K: Modell wählen und trainieren -> Mitte des Projekts
K: System in Betrieb nehmen und überwachen -> Spät im Projekt
A: Die 7 Schritte: Gesamtbild, Daten beschaffen, erkunden, vorbereiten, Modell trainieren, Fine-Tuning, Betrieb/Monitoring.

### Aufgabe
Typ: radio
F: Was bedeutet Data Drift im Produktivbetrieb?
O: Ein Programmierfehler in der Pipeline
O: *Die reale Datenverteilung verändert sich mit der Zeit, das Modell "verrottet"
O: Ein zu kleiner Trainingsdatensatz
O: Ein Fehler beim Speichern des Modells
A: Deshalb braucht produktives ML Monitoring und ggf. automatisiertes Neutraining.

### Aufgabe
Typ: radio
F: Womit persistiert man ein fertig trainiertes sklearn-Modell typischerweise?
O: Mit print()
O: *Mit joblib.dump() / joblib.load()
O: Mit pd.to_csv()
O: Modelle können nicht gespeichert werden
A: joblib ist das Standardwerkzeug zum Speichern/Laden von sklearn-Modellen.

### Aufgabe
Typ: truefalse
F: SimpleImputer(strategy='median') kann auch auf rein kategoriale Spalten sinnvoll angewendet werden.
L: false
A: Der Median ist nur für numerische Werte sinnvoll; für Kategorien nutzt man strategy='most_frequent'.

### Aufgabe
Typ: radio
F: Ein ColumnTransformer kombiniert numerische und kategoriale Pipelines wie?
O: Sequenziell nacheinander
O: *Parallel, auf jeweils festgelegten Spalten
O: Nur numerische Spalten werden verarbeitet
O: Es können keine Pipelines kombiniert werden
A: ColumnTransformer wendet unterschiedliche Pipelines parallel auf unterschiedliche Spaltengruppen an.

### Aufgabe
Typ: radio
F: Reales Beispiel California Housing: Ein Entscheidungsbaum erreicht Trainings-RMSE = 0. Was bedeutet das?
O: Ein perfektes, generalisierendes Modell
O: *Massives Overfitting
O: Ein Implementierungsfehler
O: Idealer Wert, der immer angestrebt werden sollte
A: RMSE = 0 auf Training bei einem Baum ist praktisch immer Overfitting, kein Erfolg.

## Lineare Regression, Gradientenverfahren & Regularisierung
Normalengleichung, GD-Varianten, Ridge/Lasso/Elastic Net, logistische Regression

### Aufgabe
Typ: fillblank
F: Das lineare Modell lautet ŷ = h(x) = θᵀx, wobei durch den {{Bias-Trick}} ein künstliches Merkmal x₀=1 eingeführt wird.
A: Damit lässt sich der Bias-Term kompakt im Skalarprodukt mitführen.

### Aufgabe
Typ: radio
F: Warum ist MSE als Kostenfunktion der linearen Regression gut geeignet?
O: Sie ist immer null
O: *Sie ist konvex mit genau einem Minimum
O: Sie ignoriert Ausreißer komplett
O: Sie benötigt kein Gradientenverfahren
A: Konvexität garantiert, dass Gradientenverfahren das globale Minimum findet.

### Aufgabe
Typ: radio
F: Wovon hängt die Größe der Matrix XᵀX bei der Normalengleichung ab?
O: Von der Anzahl der Datenpunkte m
O: *Von der Anzahl der Merkmale n
O: Von der gewählten Lernrate
O: Von der Anzahl der Testdaten
A: XᵀX ist eine n×n-Matrix — sie wächst mit der Merkmalszahl, nicht mit m.

### Aufgabe
Typ: radio
F: Bei Millionen Merkmalen sollte man für lineare Regression eher verwenden:
O: Die klassische Normalengleichung
O: *Ein Gradientenverfahren
O: Gar kein Training, nur Vorhersage
O: k-Nearest-Neighbors
A: Normalengleichung/SVD sind bei sehr vielen Merkmalen zu langsam (O(n^2,4) bis O(n^3)).

### Aufgabe
Typ: truefalse
F: Mit dem Gradientenverfahren findet man bei der linearen Regression garantiert nur ein lokales, nicht das globale Minimum.
L: false
A: Da MSE bei linearer Regression konvex ist, findet GD auch das globale Minimum — lokale Minima sind nur bei nicht-konvexen Problemen (z. B. Deep Learning) ein Thema.

### Aufgabe
Typ: radio
F: Was passiert bei einer zu großen Lernrate im Gradientenverfahren?
O: Das Training wird nur langsamer
O: *Es kann zur Divergenz kommen (Trainingsfehler steigt)
O: Nichts, die Lernrate hat keinen Einfluss
O: Das Modell wird automatisch robuster
A: Zu große Lernrate = Sprung über das Minimum hinweg, im schlimmsten Fall Divergenz.

### Aufgabe
Typ: checkbox
F: Welche Aussagen zu Batch-, Stochastic- und Mini-Batch-GD sind korrekt?
O: *Batch-GD nutzt bei jedem Schritt den gesamten Datensatz
O: *SGD kann leichter aus kleinen lokalen Minima entkommen
O: *Mini-Batch ist GPU-optimal
O: SGD konvergiert immer glatter als Batch-GD
A: SGD "zappelt" (hohe Varianz), Batch-GD ist glatt, Mini-Batch liegt dazwischen und ist GPU-freundlich.

### Aufgabe
Typ: radio
F: Was setzt SGD hinsichtlich der Datenreihenfolge voraus?
O: Sortierung nach Label
O: *IID-Daten (durchmischt)
O: Sortierung nach Merkmalswert
O: Keine besonderen Anforderungen
A: SGD braucht durchmischte (IID) Daten, sonst wird das Training verzerrt.

### Aufgabe
Typ: radio
F: Wie viele neue Merkmale erzeugt PolynomialFeatures(degree=d) grob (inkl. Bias) aus n Merkmalen?
O: n · d
O: *(n+d)!/(d!·n!)
O: n² + d²
O: n/d
A: Kombinatorische Explosion bei polynomialer Regression — Formel aus dem Cheatsheet.

### Aufgabe
Typ: radio
F: Lernkurven: Beide Kurven (Train/Val) liegen hoch und nah beieinander. Was bedeutet das?
O: Overfitting
O: *Underfitting
O: Perfektes Modell
O: Data Leakage
A: Hohe, nahe beieinanderliegende Fehlerkurven = Underfitting; mehr Daten helfen hier nicht.

### Aufgabe
Typ: fillblank
F: Der Verallgemeinerungsfehler setzt sich zusammen aus {{Bias}}, {{Varianz}} und dem irreduziblen Fehler.
A: Bias-Varianz-Zerlegung des Gesamtfehlers.

### Aufgabe
Typ: truefalse
F: Der statistische Bias in der Bias-Varianz-Zerlegung ist dasselbe wie der Bias-Term θ₀ des Modells.
L: false
A: Zwei unterschiedliche Konzepte trotz gleichen Namens — beliebte Verwechslungsfalle.

### Aufgabe
Typ: radio
F: Ridge-Regularisierung (L2) bewirkt, dass Gewichte...
O: exakt auf 0 gesetzt werden
O: *geschrumpft, aber nie exakt auf 0 gesetzt werden
O: unverändert bleiben
O: nur beim Testen verändert werden
A: Ridge schrumpft alle Gewichte, setzt aber keine exakt auf 0 (im Gegensatz zu Lasso).

### Aufgabe
Typ: radio
F: Welche Regularisierung eignet sich für automatische Feature-Selektion?
O: Ridge (L2)
O: *Lasso (L1)
O: Early Stopping
O: StandardScaler
A: Lasso setzt Gewichte unwichtiger Merkmale exakt auf 0.

### Aufgabe
Typ: checkbox
F: Wann ist Elastic Net dem reinen Lasso vorzuziehen?
O: *Wenn es mehr Merkmale als Datenpunkte gibt
O: *Wenn Merkmale stark korreliert sind
O: Wenn nur ein einziges Merkmal existiert
O: Nie, Lasso ist immer besser
A: In diesen Fällen wird Lasso instabil; Elastic Net (Mix aus L1/L2) ist robuster.

### Aufgabe
Typ: truefalse
F: Der Bias-Term θ₀ wird bei Ridge/Lasso/Elastic Net mitregularisiert.
L: false
A: θ₀ wird nie regularisiert (Summe läuft ab i=1).

### Aufgabe
Typ: radio
F: Was besagt "α↑ ⇒ Varianz↓, Bias↑" bei Ridge?
O: Mehr Regularisierung erhöht immer die Genauigkeit
O: *Stärkere Regularisierung senkt Varianz, erhöht aber Bias (Underfitting-Gefahr)
O: α beeinflusst nur die Trainingszeit
O: α hat keinen Effekt auf Bias/Varianz
A: Klassischer Bias-Varianz-Trade-off bei zunehmender Regularisierungsstärke.

### Aufgabe
Typ: radio
F: Was ist der Kern von Early Stopping?
O: Das Training läuft immer exakt 100 Epochen
O: *Training stoppen (oder zum besten Zustand zurückkehren), sobald der Validierungsfehler wieder steigt
O: Es ist eine Form von Datenaugmentierung
O: Es ersetzt die Notwendigkeit eines Validierungssets
A: Hinton nannte es "beautiful free lunch" — kostenlose Verbesserung durch rechtzeitiges Stoppen.

### Aufgabe
Typ: radio
F: Um das beste Zwischenmodell bei Early Stopping zu sichern, verwendet man...
O: sklearn.base.clone()
O: *copy.deepcopy()
O: pickle ausschließlich für Hyperparameter
O: Gar keine Kopie ist nötig
A: clone() kopiert nur Hyperparameter, deepcopy() sichert auch die gelernten Gewichte.

### Aufgabe
Typ: radio
F: Was ist der Hyperparameter C bei logistischer Regression/SVM?
O: Identisch mit α bei Ridge
O: *Der Kehrwert der Regularisierungsstärke (großes C = wenig Regularisierung)
O: Die Lernrate
O: Die Anzahl der Iterationen
A: C ist das Gegenteil von α: großes C = wenig Regularisierung.

### Aufgabe
Typ: radio
F: Warum kann lineare Regression nicht direkt für Klassifikation verwendet werden?
O: Sie ist zu langsam
O: *Sie kann Werte außerhalb von [0,1] liefern, was als Wahrscheinlichkeit unsinnig ist
O: Sie funktioniert nur mit einem Merkmal
O: Sie ist nicht differenzierbar
A: Deshalb transformiert die logistische Regression den linearen Score mit der Sigmoidfunktion.

### Aufgabe
Typ: fillblank
F: Die Sigmoidfunktion lautet σ(t) = 1/(1+e^{{-t}}), mit σ(0) = {{0,5;0.5}}.
A: Standard-Sigmoid, Wendepunkt bei t=0.

### Aufgabe
Typ: radio
F: Was ist der Logit?
O: Das Gegenteil der Sigmoidfunktion
O: *Der natürliche Logarithmus der Odds, ln(p/(1−p)) — Inverse der Sigmoid
O: Ein anderer Name für die Kostenfunktion
O: Die Ableitung der Sigmoidfunktion
A: Logit = Inverse Sigmoid, verbindet lineares Modell und Wahrscheinlichkeit.

### Aufgabe
Typ: radio
F: Warum nutzt man bei logistischer Regression Log Loss statt MSE?
O: MSE ist rechnerisch nicht möglich
O: *MSE kombiniert mit Sigmoid wäre nicht konvex; Log Loss ist konvex
O: Log Loss ist immer kleiner als MSE
O: Es gibt keinen inhaltlichen Grund, nur Konvention
A: Nicht-Konvexität würde lokale Minima riskieren; Log Loss garantiert ein globales Minimum via GD.

### Aufgabe
Typ: truefalse
F: Für die logistische Regression existiert eine geschlossene Normalengleichungs-Lösung wie bei linearer Regression.
L: false
A: Log Loss hat keine geschlossene Form — nur iteratives Training via GD.

### Aufgabe
Typ: radio
F: Wie viele binäre Klassifikatoren benötigt One-vs-Rest bei 10 Klassen?
O: 1
O: 45
O: *10
O: 100
A: OvR trainiert genau einen Klassifikator pro Klasse.

### Aufgabe
Typ: radio
F: Wie viele Klassifikatoren benötigt One-vs-One bei 10 Klassen?
O: 10
O: *45
O: 90
O: 100
A: OvO: n(n−1)/2 = 10·9/2 = 45 (z. B. bei MNIST und SVC relevant).

### Aufgabe
Typ: truefalse
F: Softmax eignet sich auch für unabhängige, sich nicht gegenseitig ausschließende Merkmale (z. B. innen/außen UND Tag/Nacht gleichzeitig).
L: false
A: Softmax ist nur für exklusive Klassen geeignet; für unabhängige Eigenschaften braucht man mehrere binäre Klassifikatoren.

### Aufgabe
Typ: radio
F: Was berechnet die Kreuzentropie bei Softmax-Regression im Zwei-Klassen-Fall (K=2)?
O: Etwas völlig anderes als Log Loss
O: *Dasselbe wie der binäre Log Loss
O: Immer den Wert 0
O: Nur den MSE
A: Bei K=2 ist die Kreuzentropie identisch mit dem binären Log Loss.

### Aufgabe
Typ: block
F: Ordnen Sie die Optimierungsmethode ihrer Haupteigenschaft zu.
S: Ein Rechenschritt, globales Minimum
S: Iterativ, funktioniert bei Millionen Merkmalen
S: Extrem verrauscht, entkommt lokalen Minima
K: Normalengleichung -> Ein Rechenschritt, globales Minimum
K: Batch-Gradientenverfahren -> Iterativ, funktioniert bei Millionen Merkmalen
K: Stochastic Gradient Descent -> Extrem verrauscht, entkommt lokalen Minima
A: Zusammenfassung der zentralen Eigenschaften der drei Optimierungsansätze.

## Logistische Regression & Klassifikationsmetriken
Konfusionsmatrix, Precision/Recall/F1, ROC/PR-Kurve, Schwellenwert

### Aufgabe
Typ: radio
F: Konfusionsmatrix-Konvention laut Vorlesungsfolien: Wo steht True Positive?
O: Unten rechts
O: *Oben links
O: Oben rechts
O: Unten links
A: Auf den Folien steht TP oben links — Achtung, sklearn macht das anders!

### Aufgabe
Typ: radio
F: Wie ordnet sklearns confusion_matrix() bei binärer Klassifikation standardmäßig an?
O: [[TP,FN],[FP,TN]]
O: *[[TN,FP],[FN,TP]]
O: [[TP,FP],[FN,TN]]
O: Zufällige Reihenfolge
A: sklearn ordnet die negative Klasse zuerst — die zentrale Klausurfalle.

### Aufgabe
Typ: fillblank
F: Precision (Relevanz) = TP / (TP + {{FP}}).
A: Anteil der als positiv Markierten, die wirklich positiv sind.

### Aufgabe
Typ: fillblank
F: Recall (Sensitivität, TPR) = TP / (TP + {{FN}}).
A: Anteil der tatsächlich Positiven, die auch gefunden wurden.

### Aufgabe
Typ: fillblank
F: Spezifität (TNR) = TN / (TN + {{FP}}).
A: Anteil der tatsächlich Negativen, die korrekt erkannt wurden.

### Aufgabe
Typ: fillblank
F: Fallout (FPR) = FP / (TN + FP) = 1 − {{Spezifität}}.
A: Fallout ist das Gegenstück zur Spezifität und bildet die x-Achse der ROC-Kurve.

### Aufgabe
Typ: radio
F: "Genauigkeit" ist im Deutschen der übliche Begriff für welche Metrik?
O: *Accuracy
O: Precision
O: Recall
O: Spezifität
A: Wichtige Vokabelfalle: "Genauigkeit" = Accuracy, NICHT Precision!

### Aufgabe
Typ: radio
F: Wie heißt Precision auf Deutsch (laut Kurs)?
O: Genauigkeit
O: *Relevanz (positiver Vorhersagewert)
O: Trefferquote
O: Richtig-negativ-Rate
A: Precision = Relevanz/PPV, nicht Genauigkeit.

### Aufgabe
Typ: checkbox
F: Ein Virus-Test hat TP=1, FN=1, FP=0, TN=998. Welche Aussagen stimmen?
O: *Die Accuracy liegt bei 99,9 %
O: *Der Recall liegt bei nur 50 %
O: Precision und Recall sind beide 100 %
O: Dieser Test ist trotz hoher Accuracy zuverlässig
A: Hohe Accuracy täuscht bei starker Klassenunbalance — die Hälfte der Infizierten wird übersehen.

### Aufgabe
Typ: radio
F: Ein 5-Detektor klassifiziert nur eine einzige Instanz als "5", und diese ist tatsächlich eine 5. Was folgt daraus?
O: Precision = 0 %, Recall = 100 %
O: *Precision = 100 %, Recall ist winzig
O: Precision und Recall sind beide 100 %
O: Diese Situation ist unmöglich
A: 1/1 = 100 % Precision, aber fast alle echten Fünfen sind False Negatives → winziger Recall.

### Aufgabe
Typ: checkbox
F: In welchen Szenarien ist Recall (nicht Precision) die wichtigere Metrik?
O: *Ladendieb-Erkennung
O: *Covid-Screening (günstiger Nachtest bei FP)
O: Kindervideo-Filter
O: Krebsdiagnose mit teurer Folgediagnostik
A: Wenn False Negatives (Übersehen) teuer sind, optimiert man auf Recall.

### Aufgabe
Typ: checkbox
F: In welchen Szenarien ist Precision die wichtigere Metrik?
O: *Kindervideo-Filter
O: *Krebsdiagnose (teure Folgediagnostik bei Fehlalarm)
O: Ladendieb-Erkennung
O: Covid-Screening
A: Wenn False Positives (Fehlalarm) teuer sind, optimiert man auf Precision.

### Aufgabe
Typ: radio
F: Was ist das harmonische Mittel aus Precision und Recall?
O: Accuracy
O: *F1-Score
O: Spezifität
O: AUC
A: F1 = 2PR/(P+R), bestraft niedrige Werte stark.

### Aufgabe
Typ: truefalse
F: Der F1-Score ist das arithmetische Mittel aus Precision und Recall.
L: false
A: F1 ist das harmonische, nicht das arithmetische Mittel — wichtiger Unterschied.

### Aufgabe
Typ: radio
F: Was passiert mit dem Recall, wenn man den Klassifikations-Schwellenwert erhöht?
O: Recall steigt immer
O: *Recall sinkt monoton
O: Recall bleibt konstant
O: Recall verhält sich zufällig
A: Recall ist im Schwellenwert streng monoton fallend.

### Aufgabe
Typ: radio
F: Verhält sich Precision beim Erhöhen des Schwellenwerts ebenfalls streng monoton?
O: Ja, sie steigt immer streng monoton
O: *Nein, sie kann zwischenzeitlich auch wieder sinken
O: Nein, sie bleibt immer konstant
O: Ja, sie sinkt streng monoton
A: Precision ist NICHT monoton — kann bei einzelnen fallenden TPs kurzzeitig sinken.

### Aufgabe
Typ: radio
F: Warum ist die PR-Kurve "zackig", die ROC-Kurve aber glatt/monoton?
O: Zufall, kein systematischer Grund
O: *Weil Precision nicht monoton ist, Recall/FPR aber schon
O: Weil die PR-Kurve auf weniger Daten beruht
O: Weil ROC nur bei balancierten Daten funktioniert
A: Die zugrundeliegende Nicht-Monotonie von Precision erzeugt das Zick-Zack-Muster.

### Aufgabe
Typ: radio
F: Über welche Methode liefert SGDClassifier seinen Score?
O: predict_proba()
O: *decision_function()
O: score()
O: predict_log_proba()
A: SGDClassifier hat standardmäßig keine echten Wahrscheinlichkeiten, nur einen Score via decision_function().

### Aufgabe
Typ: radio
F: Über welche Methode liefert RandomForestClassifier typischerweise Klassenwahrscheinlichkeiten?
O: decision_function()
O: *predict_proba()
O: score_samples()
O: transform()
A: Random Forest liefert Klassenanteile über predict_proba().

### Aufgabe
Typ: radio
F: Was liefert cross_val_predict() im Gegensatz zu cross_val_score()?
O: Nur einen Metrikwert je Fold
O: *Out-of-Sample-Vorhersagen für jeden Trainingspunkt
O: Ausschließlich Trainingszeiten
O: Beide liefern identische Ergebnisse
A: cross_val_predict gibt echte Vorhersagen zurück (aus dem Fold, in dem der Punkt nicht trainiert wurde) — Basis für Konfusionsmatrix/ROC.

### Aufgabe
Typ: radio
F: Was zeigt die ROC-Kurve auf ihren Achsen?
O: Precision über Recall
O: *TPR (Recall) über FPR (Fallout)
O: Accuracy über Schwellenwert
O: F1 über Precision
A: ROC = True Positive Rate über False Positive Rate.

### Aufgabe
Typ: radio
F: Was bedeutet ein AUC-Wert von 0,5?
O: Ein perfekter Klassifikator
O: *Reines Zufallsraten
O: Ein Klassifikator, der immer falsch liegt
O: Ein besonders robuster Klassifikator
A: AUC=1 perfekt, AUC=0,5 = Zufallsdiagonale.

### Aufgabe
Typ: truefalse
F: Liegt eine ROC-Kurve klar UNTER der Zufalls-Diagonale, ist der Klassifikator praktisch unbrauchbar (schlechter als Raten).
L: true
A: In diesem Fall wäre Zufallsraten dem Modell überlegen.

### Aufgabe
Typ: radio
F: Wann bevorzugt man die PR-Kurve gegenüber der ROC-Kurve?
O: Bei perfekt balancierten Klassen
O: *Wenn die positive Klasse selten ist oder FP wichtiger als FN sind
O: Niemals, ROC ist immer besser
O: Nur bei Regressionsproblemen
A: ROC/AUC wirkt bei starker Klassenunbalance oft zu optimistisch; PR-Kurve ist dann aussagekräftiger.

### Aufgabe
Typ: radio
F: MNIST besteht aus wie vielen Pixeln pro Bild?
O: 24x24 = 576
O: *28x28 = 784
O: 32x32 = 1024
O: 20x20 = 400
A: Standard-MNIST-Bildgröße, Grundwissen aus dem Praktikum.

### Aufgabe
Typ: truefalse
F: Die Labels im originalen MNIST-Datensatz (fetch_openml) sind vom Typ Integer.
L: false
A: Die Labels sind Strings ('5', nicht 5) — wichtige Praktikums-Falle.

### Aufgabe
Typ: radio
F: Was zählt für die richtige Klassenzuordnung bei precision_recall_curve() als praktisch relevante Rückgabe-Eigenschaft?
O: precisions und thresholds haben gleich viele Elemente
O: *thresholds hat ein Element weniger als precisions/recalls
O: recalls hat immer nur zwei Werte
O: Die Funktion gibt keine Arrays zurück
A: Für den theoretischen Extrempunkt (Schwelle unendlich hoch) gibt es keinen zugehörigen Schwellenwert.

### Aufgabe
Typ: radio
F: Bei einem extrem niedrigen (sehr negativen) Schwellenwert gilt für den Recall meist:
O: Recall = 0
O: *Recall = 1 (fast alles wird als positiv erkannt)
O: Recall bleibt bei 0,5
O: Recall ist nicht definiert
A: Wird praktisch alles als positiv markiert, kann kein True Positive verloren gehen → Recall=1.

### Aufgabe
Typ: radio
F: Was passiert mit Precision, wenn ein Modell bei sehr hohem Schwellenwert gar keine positive Vorhersage mehr trifft (TP=0, FP=0)?
O: Precision wird 0
O: Ein Fehler wird ausgelöst
O: *Per Konvention wird Precision auf 1 gesetzt
O: Precision bleibt beim letzten gültigen Wert
A: 0/0 wird bei precision_recall_curve() als 1 definiert (informelle "leere Wahrheit").

### Aufgabe
Typ: checkbox
F: Welche Aussagen zur Multiclass-Klassifikation stimmen?
O: *LogisticRegression, RandomForestClassifier und GaussianNB sind von Haus aus multiklassenfähig
O: *SGDClassifier und SVC benötigen eine OvR/OvO-Strategie
O: Die N×N-Konfusionsmatrix ist immer symmetrisch
O: OvO wird von SVC standardmäßig genutzt
A: Rein binäre Modelle brauchen OvR/OvO; die Multiclass-Matrix ist i. A. nicht symmetrisch (unterschiedliche Verwechslungsraten je Richtung); SVC nutzt tatsächlich OvO als Standard.

### Aufgabe
Typ: block
F: Ordnen Sie jede Formel der richtigen Metrik zu.
S: Precision
S: Recall
S: Spezifität
K: TP/(TP+FP) -> Precision
K: TP/(TP+FN) -> Recall
K: TN/(TN+FP) -> Spezifität
A: Grundformeln der Klassifikationsmetriken.

### Aufgabe
Typ: radio
F: Skalierung verbessert bei MNIST mit SGD die Accuracy von 85,8% auf ca. 89,1%. Was zeigt das?
O: Skalierung ist bei Klassifikation nie nötig
O: *Auch bei Klassifikatoren wie SGD kann Skalierung die Performance spürbar verbessern
O: Skalierung verschlechtert die Performance meist
O: Das Ergebnis ist reiner Zufall
A: Ein praktisches Beispiel für den Nutzen von Feature Scaling auch bei Klassifikationsaufgaben.

## Entscheidungsbäume & Ensemble Learning
Gini/Entropie, CART, Regularisierung, Bagging/Boosting/Random Forest

### Aufgabe
Typ: radio
F: Sind Entscheidungsbäume White-Box- oder Black-Box-Modelle?
O: *White-Box
O: Black-Box
O: Weder noch
O: Das hängt von der Tiefe ab
A: Jede Entscheidung ist Schritt für Schritt nachvollziehbar — im Gegensatz zu Random Forest/NN (Black-Box).

### Aufgabe
Typ: radio
F: Warum sind unregularisierte Entscheidungsbäume "nichtparametrisch"?
O: Sie haben gar keine Parameter
O: *Ihre Struktur passt sich frei an die Daten an, ohne feste Anzahl an Parametern vorab
O: Sie verwenden nur kategoriale Merkmale
O: Sie können nicht trainiert werden
A: Ohne Beschränkung wächst der Baum frei — Gefahr von 100% Trainings-Accuracy (Overfitting).

### Aufgabe
Typ: fillblank
F: Die Gini-Unreinheit ist definiert als G = 1 − Σp{{²;^2}}.
A: Standardformel, Default-Kriterium in sklearn.

### Aufgabe
Typ: radio
F: Welchen Wert hat die Gini-Unreinheit bei einem vollkommen reinen Knoten?
O: 1
O: 0,5
O: *0
O: Unendlich
A: Rein = nur eine Klasse vorhanden → G=0.

### Aufgabe
Typ: radio
F: Welchen Wert hat die Entropie bei perfekter 50/50-Verteilung zwischen zwei Klassen?
O: 0
O: 0,5
O: *1
O: 2
A: Bei binärer Gleichverteilung ist H=1 (Bit), G=0,5.

### Aufgabe
Typ: truefalse
F: Gini und Entropie führen praktisch fast immer zum selben Baum, weil ihr Optimum an derselben Stelle liegt.
L: true
A: Sie unterscheiden sich nur in der Skalierung; Gini wird wegen der Rechengeschwindigkeit bevorzugt.

### Aufgabe
Typ: radio
F: Was bedeutet, dass CART "greedy" arbeitet?
O: Der Algorithmus testet alle möglichen Bäume
O: *Er optimiert nur den aktuellen Split, ohne zukünftige Splits zu berücksichtigen
O: Er verwendet immer den optimalen globalen Baum
O: Er ist nur für Regressionsprobleme geeignet
A: Greedy = lokal optimale Entscheidung pro Schritt, kein garantiert global optimaler Baum.

### Aufgabe
Typ: truefalse
F: Den global optimalen Entscheidungsbaum zu finden, ist NP-vollständig.
L: true
A: Deshalb verwendet CART einen greedy-Ansatz statt exhaustiver Suche.

### Aufgabe
Typ: radio
F: Was liefert predict_proba() bei einem einzelnen Entscheidungsbaum?
O: Eine kontinuierliche, fein abgestufte Wahrscheinlichkeit
O: *Die Klassenanteile im jeweiligen Blatt
O: Immer exakt 0 oder 1
O: Den Gini-Wert des Blatts
A: Alle Punkte im selben Blatt bekommen exakt dieselbe Wahrscheinlichkeitsverteilung.

### Aufgabe
Typ: checkbox
F: Welche Hyperparameter regularisieren einen Entscheidungsbaum gegen Overfitting?
O: *max_depth
O: *min_samples_leaf
O: *max_leaf_nodes
O: n_estimators
A: n_estimators ist ein Ensemble-Parameter (z. B. Random Forest), kein Baum-Regularisierungsparameter.

### Aufgabe
Typ: fillblank
F: Merkregel zur Baum-Regularisierung: {{min}}-Parameter erhöhen, {{max}}-Parameter senken, um Overfitting zu bekämpfen.
A: min_samples_leaf/split rauf, max_depth/max_leaf_nodes runter.

### Aufgabe
Typ: truefalse
F: Skalierung der Merkmale hilft bei einem underfittenden Entscheidungsbaum.
L: false
A: Klassische Fangfrage — Skalieren hilft Bäumen nie, weder gegen Over- noch Underfitting.

### Aufgabe
Typ: radio
F: Warum sind Entscheidungsgrenzen von Bäumen "treppenförmig"?
O: Wegen der Gini-Berechnung
O: *Weil Splits immer achsenparallel erfolgen
O: Weil Bäume immer binär sind
O: Wegen der Regularisierung
A: Achsenparallele Splits können diagonale Trennungen nur approximieren.

### Aufgabe
Typ: radio
F: Was kann helfen, wenn ein Baum unter rotierten/schrägen Daten leidet?
O: Skalierung
O: *PCA als reine Drehung (ohne Dimensionsreduktion)
O: Mehr Trainingsdaten
O: Ein größeres max_depth
A: PCA kann die Daten so drehen, dass Splits wieder achsenparallel gut funktionieren.

### Aufgabe
Typ: truefalse
F: Entscheidungsbäume gelten als instabil, weil kleine Datenänderungen zu völlig anderen Bäumen führen können.
L: true
A: Diese hohe Varianz ist die Hauptmotivation für Ensemble-Methoden.

### Aufgabe
Typ: radio
F: Was ist Hard Voting?
O: Mittelung der Klassenwahrscheinlichkeiten
O: *Jeder Klassifikator stimmt für eine Klasse, Mehrheit gewinnt
O: Nur ein einziges Modell entscheidet
O: Gewichtete Fehlerkorrektur wie bei AdaBoost
A: Hard Voting = einfache Mehrheitsentscheidung ohne Wahrscheinlichkeiten.

### Aufgabe
Typ: radio
F: Was braucht ein SVC-Modell, damit es an Soft Voting teilnehmen kann?
O: kernel='linear'
O: *probability=True
O: max_iter=1000
O: Nichts Besonderes
A: Soft Voting benötigt predict_proba(), das bei SVC nur mit probability=True verfügbar ist.

### Aufgabe
Typ: radio
F: Was unterscheidet Bagging von Pasting?
O: Bagging ist sequenziell, Pasting parallel
O: *Bagging zieht mit Zurücklegen, Pasting ohne Zurücklegen
O: Pasting funktioniert nur bei Regression
O: Es gibt keinen Unterschied
A: Beide sind parallel, unterscheiden sich nur im Ziehverfahren der Teilmengen.

### Aufgabe
Typ: fillblank
F: Beim Bootstrap-Sampling sieht jeder Prädiktor im Schnitt nur etwa {{63;63%;63 Prozent}} % der Daten; der Rest heißt Out-of-Bag.
A: 1 − e^(−1) ≈ 63,2 % — die restlichen ~37 % dienen als Gratis-Validierung.

### Aufgabe
Typ: radio
F: Wofür kann man Out-of-Bag-Instanzen nutzen?
O: Für zusätzliches Training
O: *Als kostenlose Validierung ohne separates Val-Set
O: Nur für die finale Testbewertung
O: Für Data Augmentation
A: oob_score_ nutzt genau diese ungesehenen ~37% als Validierung.

### Aufgabe
Typ: radio
F: Was unterscheidet Random Forest von reinem Bagging mit Bäumen?
O: Random Forest verwendet ausschließlich lineare Modelle
O: *Random Forest sucht den besten Split zusätzlich nur in einer zufälligen Merkmalsteilmenge (~√n)
O: Random Forest ist immer langsamer
O: Es gibt keinen Unterschied
A: Zusätzlicher Zufall bei der Merkmalsauswahl je Split erhöht die Diversität der Bäume.

### Aufgabe
Typ: radio
F: Was misst feature_importances_?
O: Die Trainingszeit pro Merkmal
O: *Wie stark ein Merkmal im Schnitt zur Unreinheits-Reduktion beiträgt (Summe = 1)
O: Die Korrelation zum Zielwert
O: Die Anzahl der NaN-Werte
A: Normiertes Maß für den Beitrag eines Merkmals über alle Bäume/Knoten hinweg.

### Aufgabe
Typ: radio
F: Was macht Extra-Trees zusätzlich zufällig, im Vergleich zu Random Forest?
O: Die Zielvariable
O: *Die Schwellenwerte der Splits (statt optimaler Suche)
O: Die Anzahl der Klassen
O: Die Baumtiefe
A: Extra-Trees würfeln zusätzlich Schwellenwerte — mehr Bias, weniger Varianz, schnelleres Training.

### Aufgabe
Typ: checkbox
F: Welche Aussagen zu Boosting sind korrekt?
O: *Boosting arbeitet sequenziell, nicht parallelisierbar
O: *Boosting senkt primär den Bias
O: Boosting senkt primär die Varianz
O: Boosting ist identisch mit Bagging
A: Merksatz: Bagging senkt Varianz, Boosting senkt Bias.

### Aufgabe
Typ: radio
F: Was ist das Standard-Basismodell von AdaBoost?
O: Ein tiefer, unregularisierter Baum
O: *Ein Decision Stump (max_depth=1)
O: Ein neuronales Netz
O: Eine SVM
A: AdaBoost kombiniert klassisch viele einfache Stumps.

### Aufgabe
Typ: radio
F: Worauf trainiert Gradient Boosting jeden neuen Baum?
O: Auf den Originaldaten von vorne
O: *Auf den Residuen (Restfehlern) des bisherigen Ensembles
O: Auf zufällig vertauschten Labels
O: Nur auf den Out-of-Bag-Daten
A: Jeder neue Baum korrigiert die verbleibenden Fehler der Vorgänger.

### Aufgabe
Typ: radio
F: Ein Gradient-Boosting-Modell overfittet. Was tut man mit der learning_rate?
O: Erhöhen
O: *Senken
O: Auf 1 setzen
O: Ignorieren, learning_rate hat keinen Effekt
A: Klassische Fangfrage: Overfitting → Lernrate senken (Shrinkage erhöhen), nicht erhöhen!

### Aufgabe
Typ: radio
F: Was ist ein Vorteil von HistGradientBoosting (HGB)?
O: Es kann nur mit sehr kleinen Datensätzen arbeiten
O: *Es ist durch Binning bis zu ~100x schneller und kann mit NaN umgehen
O: Es benötigt zwingend GPU-Hardware
O: Es funktioniert nur für Regression
A: HGB nutzt Bins statt exakter Sortierung — deutlich schneller, robust gegenüber fehlenden Werten.

### Aufgabe
Typ: radio
F: Was macht ein Blender beim Stacking?
O: Er mittelt einfach alle Vorhersagen
O: *Er lernt aus den Out-of-Sample-Vorhersagen der Basismodelle die finale Vorhersage
O: Er trainiert die Basismodelle neu
O: Er ist identisch mit Hard Voting
A: Stacking nutzt einen Meta-Lerner statt trivialer Aggregation.

### Aufgabe
Typ: block
F: Ordnen Sie Verfahren ihrer Haupteigenschaft (Varianz- oder Bias-Reduktion) zu.
S: Senkt primär Varianz
S: Senkt primär Bias
K: Bagging -> Senkt primär Varianz
K: Random Forest -> Senkt primär Varianz
K: AdaBoost -> Senkt primär Bias
K: Gradient Boosting -> Senkt primär Bias
A: Zentrale Merkregel: Bagging/RF gegen Varianz, Boosting gegen Bias.

### Aufgabe
Typ: truefalse
F: Random Forest gilt trotz seiner Baum-Basis als Black-Box-Modell.
L: true
A: Im Gegensatz zum Einzelbaum ist ein ganzes Ensemble nicht mehr direkt nachvollziehbar.

## SVM & PCA
Large Margin, Kernel-Trick, C/Gamma, Hauptkomponentenanalyse

### Aufgabe
Typ: radio
F: Was bestimmt bei einer SVM die Entscheidungsgrenze?
O: Alle Trainingspunkte gleichermaßen
O: *Nur die Support-Vektoren (Randpunkte)
O: Nur die am weitesten entfernten Punkte
O: Der Mittelwert aller Punkte
A: Punkte fernab der "Straße" könnten entfernt werden, ohne das Modell zu verändern.

### Aufgabe
Typ: fillblank
F: Die Breite der SVM-"Straße" ergibt sich aus 2 geteilt durch die {{Norm;Norm des Gewichtsvektors;norm(w)}} von w.
A: Marge maximieren = Gewichtsvektor minimieren.

### Aufgabe
Typ: checkbox
F: Welche Probleme hat Hard-Margin-SVM?
O: *Funktioniert nur bei linear separierbaren Daten
O: *Sehr anfällig für Ausreißer
O: Ist immer schneller als Soft Margin
O: Benötigt keine Skalierung
A: Deshalb wird in der Praxis fast immer Soft Margin mit Slack-Variablen verwendet.

### Aufgabe
Typ: radio
F: Was bedeutet ein kleines C bei der Soft-Margin-SVM?
O: Schmale Straße, wenig Regularisierung, Overfitting-Gefahr
O: *Breite Straße, mehr Regularisierung, Underfitting-Gefahr
O: Kein Einfluss auf die Marge
O: Automatisch Kernel-Trick aktiviert
A: Kleines C = mehr Toleranz für Verletzungen = mehr Regularisierung.

### Aufgabe
Typ: truefalse
F: Ein großes C macht das SVM-Modell starrer und einfacher.
L: false
A: Großes C macht das Modell flexibler/komplexer (weniger Regularisierung), nicht starrer.

### Aufgabe
Typ: radio
F: Warum ist Skalierung bei SVMs Pflicht?
O: Nur aus Konvention, kein inhaltlicher Grund
O: *Merkmale mit großer Skala würden sonst die Richtung der Trennung dominieren
O: SVMs funktionieren ohne Skalierung technisch nicht
O: Skalierung ist nur bei linearem Kernel nötig
A: Ohne Skalierung wird der Margin in einer Richtung künstlich winzig.

### Aufgabe
Typ: radio
F: Was ermöglicht der Kernel-Trick?
O: Explizite Berechnung der Transformation φ in sehr hohe Dimensionen
O: *Berechnung des Skalarprodukts im Zielraum, ohne φ je zu berechnen
O: Verzicht auf jegliche Optimierung
O: Nur lineare Trennungen
A: Der Kernel berechnet φ(a)ᵀφ(b) direkt aus den Originalvektoren — auch bei unendlich vielen impliziten Dimensionen (RBF).

### Aufgabe
Typ: fillblank
F: Der RBF-Kernel lautet K(a,b) = exp(−{{gamma;γ}} mal dem quadrierten Abstand zwischen a und b).
A: Gamma steuert die Breite der Glockenkurve um jeden Punkt.

### Aufgabe
Typ: radio
F: Großes Gamma beim RBF-Kernel bedeutet:
O: Glatte Entscheidungsgrenze, Underfitting-Gefahr
O: *Schmale Glocken, unregelmäßige Grenze, Overfitting-Gefahr
O: Kein Effekt auf die Entscheidungsgrenze
O: Automatisch lineare Trennung
A: Merkhilfe "Gamma = Rundheit": großes Gamma → enge, zerklüftete Grenze.

### Aufgabe
Typ: checkbox
F: Eine RBF-SVM underfittet. Welche Anpassungen sind laut Klausurhinweis sinnvoll?
O: *Gamma erhöhen
O: *C erhöhen
O: Gamma und C beide senken
O: Nur den Kernel wechseln hilft
A: Beide Parameter wirken regularisierend; bei Underfitting müssen beide "gelockert" (erhöht) werden.

### Aufgabe
Typ: radio
F: Was unterscheidet LinearSVC von SVC hinsichtlich Kernel-Trick?
O: Beide unterstützen den Kernel-Trick gleichermaßen
O: *LinearSVC unterstützt keinen Kernel-Trick, SVC schon
O: Nur LinearSVC unterstützt RBF
O: SVC ist immer schneller als LinearSVC
A: LinearSVC ist auf lineare Trennung spezialisiert (schnell, kein Kernel); SVC unterstützt volle Kernel-Vielfalt.

### Aufgabe
Typ: truefalse
F: LinearSVC besitzt eine eingebaute predict_proba()-Methode.
L: false
A: Weder LinearSVC noch SVC (ohne probability=True) liefern direkte Wahrscheinlichkeiten.

### Aufgabe
Typ: radio
F: Welche Verlustfunktion verwendet die SVM typischerweise beim Training mit Gradientenverfahren?
O: Log Loss
O: MSE
O: *Hinge Loss
O: Kreuzentropie
A: Hinge Loss: max(0, 1−t·s), linear wachsend außerhalb der Marge.

### Aufgabe
Typ: radio
F: Was steuert der Parameter ε (epsilon) bei SVR?
O: Die Regularisierungsstärke
O: *Die Breite der "Straße", innerhalb derer Punkte toleriert werden
O: Die Kernel-Wahl
O: Die Anzahl der Support-Vektoren direkt
A: SVR toleriert Abweichungen innerhalb der ε-Straße ohne Bestrafung.

### Aufgabe
Typ: radio
F: Ist PCA ein überwachtes oder unüberwachtes Verfahren?
O: Überwacht
O: *Unüberwacht
O: Teilüberwacht
O: Weder noch, es ist kein ML-Verfahren
A: PCA benötigt keine Labels — rein unüberwachtes Projektionsverfahren.

### Aufgabe
Typ: radio
F: Was bedeutet "Varianz = Information" im Kontext von PCA?
O: Hohe Varianz bedeutet immer Rauschen
O: *Dimensionen mit hoher Varianz enthalten die meiste erhaltenswerte Information
O: Varianz und Information sind unabhängig voneinander
O: Nur die niedrigste Varianz ist relevant
A: PCA behält Richtungen maximaler Varianz und verwirft Richtungen mit wenig Varianz.

### Aufgabe
Typ: block
F: Ordnen Sie PCA-Attribute ihrer Bedeutung zu.
S: Richtung der Hauptkomponente
S: Absolute Varianz je Komponente
S: Anteil erklärter Varianz je Komponente
K: components_ -> Richtung der Hauptkomponente
K: explained_variance_ -> Absolute Varianz je Komponente
K: explained_variance_ratio_ -> Anteil erklärter Varianz je Komponente
A: Eigenvektor=Richtung (components_), Eigenwert=Varianz (explained_variance_), Anteil=explained_variance_ratio_.

### Aufgabe
Typ: radio
F: PCA(n_components=2) vs. PCA(n_components=0.95) — was ist der Unterschied?
O: Kein Unterschied, beide liefern 2 Komponenten
O: *Integer = feste Komponentenzahl, Float (0,1) = automatisch gewählte Anzahl für den Varianzanteil
O: Float wählt immer weniger Komponenten als Integer
O: Nur Integer-Werte sind bei PCA erlaubt
A: Klassische Verwechslungsfalle — Integer und Float bedeuten grundlegend Verschiedenes.

### Aufgabe
Typ: fillblank
F: Bei MNIST reichen bei 95 % erklärter Varianz ungefähr {{154}} statt ursprünglich 784 Komponenten.
A: Bekannte Beispielzahl aus dem Kurs.

### Aufgabe
Typ: truefalse
F: inverse_transform() bei PCA liefert exakt das Originalbild zurück, ohne jeglichen Informationsverlust.
L: false
A: Es ist nur eine Näherung; der Rekonstruktionsfehler entspricht der weggeworfenen Varianz.

### Aufgabe
Typ: checkbox
F: Welche typischen Anwendungen hat PCA?
O: *Kompression / Beschleunigung des Trainings
O: *Visualisierung in 2D/3D
O: *Rauschfilterung
O: Perfekte verlustfreie Bildspeicherung
A: PCA ist immer mit Informationsverlust verbunden — auch bei Rauschfilterung/Kompression.

### Aufgabe
Typ: radio
F: Warum versagt PCA beim Swiss-Roll-Datensatz für Visualisierungszwecke?
O: PCA funktioniert nur bei 2D-Daten
O: *PCA ist linear und kann gekrümmte Manifolds nicht sinnvoll abbilden
O: Der Datensatz hat zu wenige Punkte
O: PCA benötigt zwingend Labels
A: Für gekrümmte Strukturen sind LLE oder t-SNE besser geeignet (nur Visualisierung, keine Rücktransformation bei t-SNE).

### Aufgabe
Typ: truefalse
F: Vor einem CNN sollte man Bilddaten routinemäßig mit PCA vorverarbeiten.
L: false
A: PCA würde die räumliche Bildstruktur zerstören — vor CNNs wird PCA nicht eingesetzt.

### Aufgabe
Typ: radio
F: Was ist der "Fluch der Dimensionalität"?
O: Zu wenige Trainingsdaten führen immer zu Fehlern
O: *In hochdimensionalen Räumen sind Daten dünn besetzt, was Overfitting begünstigt
O: Hohe Dimensionalität verbessert automatisch die Modellgüte
O: Ein Phänomen, das nur bei Bildern auftritt
A: Mit steigender Dimension wächst der benötigte Datenumfang exponentiell.

### Aufgabe
Typ: radio
F: Worauf basiert die praktische Berechnung der Hauptkomponenten in sklearn?
O: Direkte Eigenwertzerlegung der Rohdaten
O: *Singulärwertzerlegung (SVD), sklearn zentriert automatisch
O: Zufällige Stichprobenziehung
O: Gradientenverfahren
A: sklearn nutzt SVD und zentriert die Daten automatisch (bei eigener np.linalg.svd-Implementierung muss man das selbst tun).

### Aufgabe
Typ: radio
F: Warum darf PCA nicht vor dem Train-Test-Split angewendet werden?
O: PCA funktioniert nur nach dem Split technisch
O: *Das wäre Data Leakage — PCA muss nur auf Trainingsdaten gefittet werden
O: Es gibt keinen Grund, beides ist gleichwertig
O: PCA verändert die Zielvariable
A: Wie bei jedem Transformer: fit nur auf Train, transform auf Test.

### Aufgabe
Typ: checkbox
F: Welche Eigenschaften hat die SVM im Vergleich zu anderen Modellen (laut Kurs)?
O: *Gut geeignet für kleine bis mittelgroße, komplexe Datensätze
O: *Funktioniert auch bei mehr Dimensionen als Datenpunkten
O: Sehr effizient bei sehr großen Datenmengen
O: Liefert immer direkte Wahrscheinlichkeiten
A: SVM wird bei sehr großen Datenmengen ineffizient (v. a. mit Kernel); Wahrscheinlichkeiten nur mit Zusatzaufwand.

### Aufgabe
Typ: radio
F: Was passiert bei einer RBF-SVM mit einem sehr kleinen Gamma?
O: *Eine glatte, eher lineare Entscheidungsgrenze mit Underfitting-Gefahr
O: Eine zerklüftete, um einzelne Punkte geschlängelte Grenze
O: Der Kernel-Trick wird deaktiviert
O: Automatisch werden mehr Support-Vektoren gewählt
A: Kleines Gamma = breite Glocken = glatte, tendenziell zu einfache Grenze.

### Aufgabe
Typ: radio
F: Ein RBF-SVM-Modell overfittet deutlich. Was ist eine sinnvolle Gegenmaßnahme?
O: Gamma und C erhöhen
O: *Gamma und/oder C senken
O: Nur den Datensatz vergrößern hilft, Parameter anpassen ist wirkungslos
O: Auf den linearen Kernel kann man dabei nie zurückgreifen
A: Overfitting bei RBF-SVM wird durch Senken von Gamma und/oder C bekämpft (mehr Regularisierung).

### Aufgabe
Typ: truefalse
F: Bei der PCA-Rekonstruktion (inverse_transform) entspricht der Rekonstruktionsfehler genau der Varianz, die durch die Dimensionsreduktion verloren ging.
L: true
A: Rekonstruktionsfehler = weggeworfene Varianz — direkte Konsequenz der PCA-Projektion.

## Neuronale Netze — Grundlagen
Neuron, Aktivierungsfunktionen, Backprop, Loss-Wahl, Keras-Workflow

### Aufgabe
Typ: radio
F: Was berechnet der lineare Teil eines künstlichen Neurons?
O: Eine Aktivierungsfunktion
O: *Eine gewichtete Summe der Eingänge plus Bias (Skalarprodukt)
O: Den Gradienten
O: Die Konfusionsmatrix
A: z = wᵀx + b, danach folgt die nichtlineare Aktivierung.

### Aufgabe
Typ: radio
F: Was ist eine TLU (Threshold Logic Unit)?
O: Ein moderner Aktivierungsfunktionstyp
O: *wᵀx+b, gefolgt von einer Stufenfunktion
O: Ein Optimierungsalgorithmus
O: Ein Pooling-Verfahren
A: TLU ist das Grundbauteil des klassischen Perzeptrons.

### Aufgabe
Typ: truefalse
F: Ein Perzeptron kann das XOR-Problem lösen.
L: false
A: Ein einlagiges Perzeptron kann NICHT XOR lösen (Minsky/Papert 1969) — ein MLP kann es.

### Aufgabe
Typ: radio
F: Was unterscheidet Perzeptron und logistische Regression strukturell?
O: Nichts, sie sind identisch
O: *Perzeptron nutzt eine harte Stufenfunktion, logistische Regression eine differenzierbare Sigmoid
O: Logistische Regression hat keine Gewichte
O: Perzeptron kann keine linearen Grenzen lernen
A: Beide sind strukturell ähnlich (1 Neuron), unterscheiden sich in der Aktivierungsfunktion.

### Aufgabe
Typ: fillblank
F: Ab ca. {{3}} oder mehr Schichten spricht man von Deep Learning.
A: Wiederholung der zentralen Kapitel-1-Definition.

### Aufgabe
Typ: radio
F: Was bedeutet "klein x" im Vergleich zu "groß X" in der NN-Notation?
O: x ist die Zielvariable, X die Vorhersage
O: *x ist ein einzelner Datenpunkt (Merkmalsvektor), X die gesamte Datenmatrix
O: Beide sind identisch
O: x ist ein Hyperparameter
A: Explizit als Verständnisfrage im Kurs angekündigt.

### Aufgabe
Typ: radio
F: Was ist bei einem MLP durch die Aufgabenstellung fest vorgegeben?
O: Die Anzahl der Hidden Layer
O: *Die Anzahl der Input- und Output-Neuronen
O: Die Aktivierungsfunktion der Hidden Layer
O: Die Lernrate
A: Input = Merkmalszahl, Output = Klassenzahl; nur Hidden Layer sind frei wählbar.

### Aufgabe
Typ: fillblank
F: Die Sigmoid-Ableitung hat ihr Maximum bei {{0,25;0.25}}.
A: max σ'(x) = 0,25 bei x=0 — Ursache für Vanishing Gradient bei tiefen Netzen.

### Aufgabe
Typ: radio
F: Was ist das Vanishing-Gradient-Problem?
O: Der Trainingsfehler wird null
O: *Die Ableitungen werden bei Backprop über viele Schichten multipliziert und dadurch extrem klein
O: Zu wenige Trainingsdaten
O: Ein reines Regularisierungsproblem
A: Bei sättigenden Aktivierungen wie Sigmoid schrumpft der Gradient exponentiell mit der Netztiefe.

### Aufgabe
Typ: checkbox
F: Welche Gegenmittel gegen Vanishing Gradient wurden im Kurs genannt?
O: *ReLU statt Sigmoid/Tanh verwenden
O: *Eingangsmerkmale normalisieren
O: Immer alle Gewichte auf 0 initialisieren
O: Die Lernrate ignorieren
A: ReLU reicht den Gradienten unverändert durch (Faktor 1 statt max. 0,25).

### Aufgabe
Typ: radio
F: Warum werden Gewichte niemals alle mit 0 initialisiert?
O: Aus Performance-Gründen
O: *Symmetrieproblem: alle Neuronen würden sich identisch verhalten
O: sklearn/Keras verbietet das technisch
O: Bias-Werte müssten dann auch ungleich 0 sein
A: Zufällige Initialisierung bricht die Symmetrie; Bias darf dagegen 0 sein.

### Aufgabe
Typ: radio
F: Was ist die Standard-Empfehlung für die Aktivierungsfunktion in Hidden Layers?
O: Sigmoid
O: Tanh
O: *ReLU
O: Softmax
A: "Wenn Sie nicht wissen, welche Aktivierungsfunktion: nehmen Sie ReLU."

### Aufgabe
Typ: radio
F: Was ist ein Nachteil von ReLU?
O: Sie ist zu rechenintensiv
O: *Mögliche "tote Neuronen" bei dauerhaft negativem Input (Ableitung=0)
O: Sie kann keine positiven Werte ausgeben
O: Sie ist nicht differenzierbar für x>0
A: Leaky ReLU behebt dieses Problem durch eine kleine Steigung im negativen Bereich.

### Aufgabe
Typ: radio
F: Warum kollabiert ein tiefes Netz ohne nichtlineare Aktivierung zu einer einzigen linearen Funktion?
O: Weil die Gewichte dann immer 0 sind
O: *Weil die Verkettung linearer Funktionen wieder eine lineare Funktion ergibt
O: Weil Backpropagation das verhindert
O: Das passiert nur bei Sigmoid
A: Ohne Nichtlinearität bringt jeder zusätzliche Layer keinen Mehrwert.

### Aufgabe
Typ: radio
F: Wofür wird Softmax typischerweise im Output-Layer eingesetzt?
O: Bei unabhängigen Multilabel-Aufgaben
O: *Bei sich gegenseitig ausschließenden Klassen (Multiclass)
O: Bei reiner Regression
O: Nur bei binärer Klassifikation
A: Softmax erzwingt eine Wahrscheinlichkeitsverteilung über exklusive Klassen (Summe=1).

### Aufgabe
Typ: block
F: Ordnen Sie Aufgabentyp und passende Ausgabeschicht/Loss zu.
S: Regression
S: Binäre Klassifikation
S: Multiclass mit Integer-Labels
K: 1 Neuron, keine Aktivierung, mse -> Regression
K: 1 Neuron, Sigmoid, binary_crossentropy -> Binäre Klassifikation
K: n Neuronen, Softmax, sparse_categorical_crossentropy -> Multiclass mit Integer-Labels
A: Zentrale Loss/Ausgabeschicht-Zuordnung, extrem klausurrelevant.

### Aufgabe
Typ: radio
F: Wann verwendet man categorical_crossentropy statt sparse_categorical_crossentropy?
O: Wenn die Labels als Integer vorliegen (z. B. 3)
O: *Wenn die Labels bereits One-Hot-codiert sind
O: Nur bei binärer Klassifikation
O: Nie, beide sind identisch
A: sparse = Integer-Labels, ohne sparse = One-Hot-Vektoren.

### Aufgabe
Typ: checkbox
F: Welche Schritte gehören zum Backpropagation-Ablauf, in korrekter Grundidee?
O: *Vorwärtsdurchlauf mit Speichern der Zwischenergebnisse
O: *Fehler mit der Verlustfunktion messen
O: *Rückwärtsdurchlauf per Kettenregel
O: Zufälliges Neu-Labeln der Trainingsdaten
A: Backprop = Forward Pass + Cache → Loss → rückwärts Kettenregel → Gewichts-Update.

### Aufgabe
Typ: radio
F: Wie berechnet sich die Parameterzahl einer Dense-Schicht?
O: Nur Anzahl der Neuronen
O: *Eingänge · Neuronen + Neuronen (für Bias)
O: Eingänge + Neuronen
O: Eingänge² · Neuronen
A: Beispiel: 784→300 ergibt 784·300+300 = 235.500 Parameter.

### Aufgabe
Typ: radio
F: Wie viele Parameter hat eine Dense-Schicht von 300 auf 100 Neuronen?
O: 30.000
O: *30.100
O: 300.100
O: 100.300
A: 300·100 + 100 = 30.100.

### Aufgabe
Typ: truefalse
F: Ein Flatten-Layer besitzt trainierbare Parameter.
L: false
A: Flatten, Pooling und Dropout haben 0 Parameter — sie transformieren nur die Daten.

### Aufgabe
Typ: radio
F: Was sind die Keras-Standardwerte, wenn epochs und batch_size nicht angegeben werden?
O: epochs=10, batch_size=64
O: *epochs=1, batch_size=32
O: epochs=100, batch_size=1
O: epochs=1, batch_size=1
A: Wichtige Stolperfalle — ohne explizite Angabe trainiert man nur eine einzige Epoche.

### Aufgabe
Typ: radio
F: In welcher Reihenfolge gibt model.evaluate() seine Werte zurück?
O: Zuerst die Metrik, dann der Loss
O: *Zuerst der Loss, dann die Metrik(en)
O: Alphabetisch sortiert
O: Es kommt nur ein einziger Wert zurück
A: Reihenfolge: loss, dann metrics (z. B. accuracy).

### Aufgabe
Typ: radio
F: Warum werden Pixelwerte vor dem Training meist durch 255 geteilt?
O: Um die Bildgröße zu ändern
O: *Um die Werte auf den Bereich [0,1] zu normalisieren
O: Um Graustufenbilder zu erzeugen
O: Das ist rein optional und ohne Effekt
A: Normalisierung erleichtert das Training erheblich (u. a. gegen Vanishing Gradient).

### Aufgabe
Typ: radio
F: Was gilt als der wichtigste Hyperparameter eines neuronalen Netzes?
O: Die Batchgröße
O: *Die Lernrate
O: Die Anzahl der Epochen
O: Die Anzahl der Neuronen in der letzten Schicht
A: Laut Kurs: Lernrate ist der einflussreichste Hyperparameter.

### Aufgabe
Typ: truefalse
F: Mehr Schichten bringen tendenziell mehr als einfach mehr Neuronen in einer einzigen Schicht.
L: true
A: Tiefe Netze sind parametereffizienter, weil sie hierarchische Merkmale lernen können.

### Aufgabe
Typ: radio
F: Was zeigt "None" in der Output-Shape-Spalte von model.summary()?
O: Einen Fehler im Modell
O: *Eine beliebige/variable Batchgröße
O: Dass die Schicht 0 Parameter hat
O: Dass kein Bias verwendet wird
A: None steht für die flexible erste Dimension (Batchgröße), nicht für einen Fehler.

### Aufgabe
Typ: radio
F: Welche Loss-Funktion passt zu einer reinen Regressionsaufgabe mit einem Ausgabe-Neuron ohne Aktivierung?
O: sparse_categorical_crossentropy
O: binary_crossentropy
O: *mse
O: categorical_crossentropy
A: Regression: 1 Neuron, keine Aktivierung, mse (oder MAE/Huber bei Ausreißern).

### Aufgabe
Typ: checkbox
F: Welche Aussagen zum Forward Pass eines MLP sind korrekt?
O: *Er wendet die Layer-Gleichung Schicht für Schicht von links nach rechts an
O: *Zwischenergebnisse werden für den späteren Rückwärtsdurchlauf zwischengespeichert
O: Er berechnet direkt die Gewichtsänderung
O: Er läuft grundsätzlich von der letzten zur ersten Schicht
A: Forward Pass geht vorwärts inkl. Caching; die eigentliche Gewichtsanpassung erfolgt erst im Rückwärtsdurchlauf.

### Aufgabe
Typ: truefalse
F: Bei einem Multilabel-Problem (mehrere unabhängige Ja/Nein-Ausgaben) verwendet man im Output-Layer Softmax.
L: false
A: Bei Multilabel verwendet man pro Neuron eine Sigmoid-Aktivierung, nicht Softmax (das wäre nur für exklusive Klassen korrekt).
