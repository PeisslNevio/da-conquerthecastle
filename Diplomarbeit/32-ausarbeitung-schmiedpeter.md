# Teilaufgabe Schüler Schmiedpeter
\textauthor{Schmiedpeter}

## Blender

### Einleitung in Blender

#### Möglichkeiten

Blender ist ein Programm mit vielen Möglichkeiten. Zum einen kann man mit diesem Programm Modellieren außerdem hat diese eine Zeichenfunktion, sowie einen Python Editor. Schon bestehende Modelle kann man Animationen hinzufügen folgend dazu ist es eine nützliche Weise so Videos zu rendern und schneiden.

#### Basics der Modelierung

Aufgebaut ist Blender so: in der Mitte ist ein Koordinatensystem, hier passiert das meiste, links davon sind Werkzeuge. Auf der rechten Seite befinden sich die Objekt Hierache bei den man alle Ordner inkl. Kamera und Licht bzw. auch alle Objekte sieht, sowie im unteren Bereich jegliche Module wie Modifier, Material und Physiks.

![Koordinatensystem [@blender]](img/schmiedpeter/Defaultscreen-blender.png){width=90%}

In der Modellierungsansicht gibt es 3 Modi alle haben eine andere Bedeutung

- Objektmodus ist hauptsächlich für den Umgang mit mehrere Objekten und dem einfügen von Objekten. Vom Programm bereit gestellte Objekte sind der Würfel, Quader, Zylinder, die Kugel und viele mehr. Standard gemäß sind diese auf die Größe 1 Meter gesetzt und am `Set Origin` gesetzt, welches man beides gleich ändern kann. Außerdem wird dieser Modus für Module wie Physiks oder Modifier verwendet.
  Die wichtigsten Werkzeuge sind Objekte bewegen/rotieren/skalieren
  
- Der Editmodus ist ein wenig anders, dieser ist nämlich da um einzelne Objekte zu verändern

  > Der Modus funktioniert auch mit meheren Objekten, es ist nur nicht erwünscht weil ungewollte Fehler auftretten können. Aus diesem Grund sollten Objekt vor den ändern  im Editmode gruppieren.


  Auswählen funktioniert anders als im Objektmodus hier wählt man nicht ein Objekt aus sondern es hängt ab welche Ansicht ausgewählt ist. Standard ist die Punktansicht ausgewählt, hierbei können nur Ecken angewählt werden. Nach dem gleichen Prinzip funktioniert die Kanten- und Flächenansicht. *Tipp mit `Shift` kann man mehrere auswählen und mit `Str` wählt Blender alle aus, die auf der Bahn zum erst ausgewählten*.
  Wichtige Werkzeuge sind Loop Cuts und das Messer (mit diesen beiden fügt mann Kanten hinzu), bewegen, Flächen verkleinern und extrahieren bzw. füllen

- Skulptur Modus verwendet Werkzeuge, die Polys in verschiedene Art und Weisen bewegen. Das einzige Problem dabei ist, das die Polys die bewegt wurden nicht nach genauen Massen bewegt werden können. Außerdem ist zu achten, dass das Objekt mehr Polys haben soll, ansonsten wird das Entergebnis nicht den Erwartungen ersprechen.

Als Unterstützung in den jeweiligen Modus existiert dem Tool Anmerkungen. Mit diesem Tool kann man Sachen in der Eigenen Perspektive zeichnen. Im Edit und Objektmodus kann man zusätzlich auch das Tool Messen verwenden. Dieser funktioniert auch wieder in der eigenen Perspektive und ist wie Anmerkungen 2D. 
  
### Konkurrenz

Neben Blender hätte man sich noch für andere Modellierungsprogramme entscheiden können Beispielsweise *Tinkercad, AutoDesk Fusion oder OpenSCAD*. 

- Tinkercad kennt man vorallem auch durch das Entverwerfen von einfachen Schaltkreisen online und so in etwa ist es bei deren Programm für das Modellieren.
  Das Programm ist sehr simple und leicht zu verstehen - Perfekt für Anfänger
  Aber nicht geeignet für die Diplomarbeit, weil man extreme Einschränkungen hat. Man kann keine Modelle im Nachhinein abrunden, da Tinkercad nur an vorgefertigte Objekte zum Bewegen hat. Diese Modelle sind fix gefertigt und nicht veränderbar.

- AutoDesk Fusion ist spezialiesiert auf die Produktion bzw. auf Werkzeug und Maschinen. Das heißt aber nicht das dieses Programm nicht geeignet ist für das Modelieren 
  AutoDesk hat eine einfacher Handhabung *Zitat aus dem Video*. Aus iesem Grund verwenden dieses Tool sehr viele größere Firmen, wie: Yamaha und Toyota *- so deren Homepage*
  Nachteil ist das Programm kostet viel .

- OpenSCAD ist ein Open-Source  Program für das Modellieren per Code. Aus diesem Grund ist dieses Programm nicht geeignet für ein großes Projekt, wegen der hohen Komplexität.



### Nützliche Befehle

- **`Shift + A`**: Objekt hinzufügen. Weitere erklärung: /.
- **`X`**: Löschen. Weitere erklärung: Wenn man etwas löschen will kommt eine Bestätigung abfrage.
- **`TAB`**: Wechselt den Modus. Weitere erklärung: Von Objekt- auf Editmodus und zurück.
- **`LEERZEICHEN`**: Zeitleiste abspielen/ stoppen. Weitere erklärung: /.

bei den nächsten Befehle gilt:

- bei zusätzlichen Achsen Tippen `X`/`Y`/`Z` wird diese prioriesiert, mit 2x Tippen unprioriesieren
- bei `Shift` werden in Blocken bewegt

- **`G`**: verschieben im Koordinatesystem. Weitere erklärung: /.
- **`R`**: drehen. Weitere erklärung: Um den Ursprung (Oranger Punkt).
- **`S`**: skalieren. Weitere erklärung: Um den Ursprung.

Für den Objektmodus

- **`Str + J`**: Objekte gruppieren. Weitere erklärung: Funktioniert bei 2 oder mehr Objekte. Das der Befehl durchgesetzt werden kann, muss ein primär Objekt ausgewählt werden, für z.B den Ursprung des Objektes.
- **`Rechts Klick` + Ursprung ändern**: versetzt den Ursprung. Weitere erklärung: Entweder nach Masse, Volumen oder nach dem Set Origin.
- **`Rechts Klick` + Weich schattieren**: Ecken abrunden. Weitere erklärung: ohne Polys hinzufügen.

Für den Editmodus

- **`M`**: Punkte zusammenfügen. Weitere erklärung: Funktioniert bei 2 oder mehr Punkten bzw. auch bei Kanten und Flächen setzen diese aber in Punkte um. Entweder auf dem ersten/ letzten ausgewählten Punkte, in der Mitte oder beim Set Origin.
- **`Str + R`**: Loop Cuts. Weitere erklärung: Erstellt Kanten die sich um ein ganzes Objekt schlingt. Dazu kann man einstellen wie viele Schleifen erstellt werden.
- **`K`**: Messer. Weitere erklärung: fügt Schnitte zu einen Objekt hinzu. Wird `Shift` gedrückt wird der Schnitt zentral gerichtet.
- **`E`**: Extrahieren. Weitere erklärung: erweitert Flächen bzw. Kanten.
- **`I`**: Einsetzten von Flächen. Weitere erklärung: erzeugt ein kleinere Fläche in einer größeren.
- **`F`**: Füllen von Flächen und Kanten. Weitere erklärung: Bei 2 Punkte wird eine Kante erstellt ansonsten ein Fläche. Bei 5+ Punkte füllen werden oft komische Flächen erzeugt, vor allem für das Rendern und Exportieren ist das wichtig.
- **`Str + T`**: Fläche zu Dreieck konventieren. Weitere erklärung: Trifft zu alle ausgewällten Flächen und ist sinnvoll für das Exportieren bzw. Rendern.


## Erweiterte Funktionen in Blender

### Material

Das Material beschreibt das Aussehen eines Objektes bzw. einzelne Flächen - dazu gehört die Farbe, die Metalleffekt, die Rauheit und einiges mehr was definiert werden kann. Standard gemäß ist das Material ohne besondere Werte und in ein helles Grau. Das hat den Grund da Effekte bzw. Farben sonst beim Modelieren im Weg ist.

![Matterial erklärung [@blender]](img/schmiedpeter/Material_blender.png){width=90%}

Objekte sind nur einfärbbar im Editmodus. Einzelne Flächen kann man nur Farben hinzu fügen, wenn diese ausgewählt musst die Farbe auch ausgewählt werden und dann zugewiesen werden. Um die Farbe sehen zu können muss man die Ansichtsfenster Shading auf Materialbeispiel bzw gerendert ändern.



### Modifyers

sind Erweiterungen die eigene Funktionen haben, davon existieren viele. Für ein Projekt werden oft nur eine handvoll verwendet. Manche sind davon Erleichterung, das heißt auch möglich ohne Modifiers aber nur komplexer, manche davon sind komplett eigene Funktionen.  Modifyers sind auf der rechten Seite unter dem Schraubenschlüssel. Sie sind in Kategorieen auf geteilt wichtig sind hierbei Erzeugen und Physik. Zu Beachten ist es wird zuerst nur eine Übersicht erstellt. Bearbeiten kann man diese Übersicht erst wenn man diese angewendet hat. Einer der wichtigsten Modifyer sind Boolean, Mirror und collition

#### Boolean

Dieser schneidet ein Objekt von einem anderen herraus. Hierbei hängt es ab was ausgewählt wird **Schneiden, Vereinigung und Differenz**. Es ist notwendig einen Primären Körper zu haben und einen Sekundären.

#### Mirror

spiegelt das Objekt in die jeweilige Richtung die man Ausgwählt hat. Gespiegelt wird das Objekt nicht in der Mitte sondern um den Ursprung. Dieser wird als Mitte angesehen.

#### Physik

Physik ist nicht wie die anderen ein einziger Modifyer sondern gleiche eine Kategorie. Hier reagieren die Modifiers auf die Regeln der echten Welt. Möglich sind Simulationen, wie mit Flüssigkeiten oder mit Stoffen. Besonders für diese Kategorie ist auch das diese auch eine eigene Übersicht hat. Wichtig für die meisten Modifyers in dieser Kategorie einen zweites Objekt mit dem Modifyer Kollision. Dieser ist dafür da, dass Objekte mit seiner Hitbox reagieren können. Ansonsten wird dieser ignoriert, als wäre der nicht dagewesen. 
Beispiel an einem Modifyer ist das Gewebe Modifyer. Dieser funktioniert wie eine Decke. Führt man die Simlation  mit `LEERZEICHEN`  aus dann fällt der Körper hinunter. Ist ein Objekt im weg mit Kollision, dann hällt dieser hin beim fallen auf. Das Objekt kann allerdings nur zerfallen bei Eckpunkten, weil jede Fläche ist starr. In den Einstellungen ist zum Setzen wie gut das Objekt zerfällt bzw. auch wie schwer sie ist. Beim Anwenden diesem Modifyer wird der Körper in dieser Lager fixiert.



## Animationen
### Zweck und Nutzen von Animationen
Animationen sind notwendig, um statische Modelle in glaubwürdige, lesbare und emotionale Figuren zu verwandeln. In Spielen und Visualisierungen übernehmen sie mehrere Aufgaben: Sie machen Handlungen verständlich (z. B. Gehen, Angreifen), stärken die Identität einer Figur durch charakteristische Bewegungen und unterstützen die Spielmechanik durch klare Rückmeldungen (z. B. Treffer, Ausweichen). Ohne Animationen bleibt ein Modell reiner Blickfang, aber es kann keine Handlung vermitteln und wirkt technisch wie dramaturgisch unvollständig.

### Grundlagen des Rigging mit Armature
Die Armature ist das Skelett einer Figur. Sie besteht aus Knochen (Bones), die hierarchisch verbunden sind und die spätere Bewegung definieren. Jeder Knochen besitzt einen Kopf und ein Ende; aus der Ausrichtung ergibt sich die lokale Achse, die für Rotationen entscheidend ist. Damit eine Armature sauber funktioniert, müssen Skalen der Meshes angewendet sein und die Bone-Orientierungen konsistent angelegt werden.

**Parent-Knochen (Elternknochen)** bestimmen die Hierarchie. Bewegungen eines Elternknochens wirken auf alle darunterliegenden Kinderknochen. Dadurch lassen sich Ketten wie Wirbelsäule, Arm oder Bein logisch aufbauen. Ein Unterarm ist z. B. Kind des Oberarms, sodass eine Rotation des Oberarms die gesamte Kette mitführt.

![Armature-Struktur einer Figur](img/schmiedpeter/Armature.png){width=80%}

**Keep Offset** entstehen, wenn ein Knochen einem Elternknochen zugewiesen wird, seine aktuelle Position jedoch beibehält. Das bedeutet: Die Hierarchie wirkt, aber der Kindknochen verschiebt sich beim Parenten nicht an den Kopf des Elternknochens. Diese Variante ist sinnvoll, wenn der Abstand zwischen Knochen bewusst erhalten bleiben soll, z. B. bei Zubehör, Sekundärbewegungen oder technischen Rigs. Erstellt wird dies im Pose- oder Edit-Mode durch Auswahl von Kind und Elternknochen und anschließend `Str + P` mit der Option Keep Offset. So bleibt der Abstand erhalten, die Vererbung der Bewegung ist aber aktiv.

![Keep Offset im Parenting-Vergleich](img/schmiedpeter/KeepOffset.png){width=80%}

**Inverse Kinematik (IK)** wird eingesetzt, wenn man das Ende einer Knochenkette direkt steuern möchte, z. B. Hände, Füße oder ein Knie beim Aufsetzen auf den Boden. Im Gegensatz zur Vorwärtskinematik (FK), bei der jeder Knochen einzeln rotiert wird, berechnet IK die Winkel der gesamten Kette automatisch, damit das Endglied ein Ziel erreicht. Technisch wird dazu ein Ziel-Objekt (IK-Target) definiert und ein IK-Constraint auf den Endknochen gesetzt; eine Kettenlänge bestimmt, wie viele Knochen beeinflusst werden. So lassen sich stabile Kontaktpunkte erzeugen, etwa wenn eine Hand eine Waffe hält oder ein Fuß sauber am Boden bleibt.

### Anwendung an Figuren: Vorgehensweise
Für die Anwendung an einer Figur wird ein Mesh benötigt, eine Armature und eine klare Bindung zwischen beiden. Ziel ist es, dass die Knochenbewegung das Mesh nachvollziehbar verformt, ohne sichtbare Artefakte zu erzeugen. Eine Abbildung kann hier optional den Aufbau von Mesh, Armature und Gewichtung verdeutlichen.


Benötigte Schritte:
1. Mesh vorbereiten (Skalierung anwenden, Ursprung setzen).
2. Armature platzieren und Knochen entlang der geplanten Bewegung anordnen.
3. Parenting zwischen Mesh und Armature herstellen.
4. Gewichte (Weights) pruefen und bei Bedarf korrigieren.

Gerade bei organischen oder flexiblen Objekten ist die Verteilung der Gewichte entscheidend, da zu harte Uebergaenge die Bewegung unnatuerlich wirken lassen.

![Armature im Mesh (On-Figure Ansicht)](img/schmiedpeter/OnFigure.png){width=80%}

### Gewichtung und Bindung des Meshes
Das Verbinden von Mesh und Armature erfolgt in Blender über das Parenting. Dabei gibt es mehrere Modi, die das Grundgerüst der Gewichtung erzeugen und den Startpunkt fuer die spaetere Feinabstimmung liefern:

**Automatic Weights**: Blender berechnet die Gewichte automatisch anhand der Nähe zu den Knochen. Dieser Modus ist effizient und liefert oft brauchbare Ergebnisse, ist jedoch bei komplexen Formen fehleranfällig. Typische Probleme sind ungewollte Verzerrungen, wenn Knochen zu nah an anderen Bereichen liegen. Deshalb ist eine anschließende manuelle Korrektur in den Weight-Painting-Modi fast immer notwendig. In der Praxis gilt: Automatic Weights sind der Startpunkt, nicht der Abschluss.

**With Empty Groups**: Erzeugt nur die notwendigen Vertex-Gruppen ohne Gewichte. Dieser Modus ist sinnvoll, wenn die Gewichtung bewusst manuell angelegt werden soll, etwa bei technischen oder sehr klar strukturierten Modellen.

**With Envelope Weights**: Nutzt die Bone-Envelopes (Einflussbereiche) anstelle von Distanzberechnung. Der Vorteil liegt in der direkten Kontrolle über Einflussradien, allerdings ist die Methode weniger präzise bei feineren Strukturen und erfordert eine saubere Envelope-Konfiguration.

**Bone-Parenting (Bone)**: Das Mesh wird einem einzelnen Knochen untergeordnet. Diese Methode eignet sich für starre Objekte (z. B. Waffen, Schilder) und lässt keine organische Deformation zu.

![Gewichtungs-Vergleich bei auswahl der Knoche](img/schmiedpeter/Gewichtungen.png){width=80%}

Nach dem Parenting werden die Gewichte mit den Gewichtungstools (Weight Paint) verfeinert. Sie steuern, wie stark ein Knochen einzelne Punkte des Meshes beeinflusst. Jeder Vertex erhält 
Gewichte in sogenannten Vertex-Gruppen, typischerweise mit Werten zwischen 0 und 1. Ein Wert von 1 bedeutet volle Beeinflussung durch den Knochen, ein Wert von 0 keine. In der Praxis werden die Gewichte über Pinselwerkzeuge gemalt, geglättet oder normalisiert, damit Übergänge weich bleiben und sich die Summe der Einflüsse pro Punkt sinnvoll verteilt. So entstehen organische Deformationen, ohne dass das Mesh unerwünscht einbricht oder sich verzieht.

Wichtige Werkzeuge sind Add (Gewichte erhöhen), Subtract (Gewichte reduzieren), Blur oder Smooth (Übergänge glätten) sowie Normalize/Normalize All (Gewichte pro Vertex ausgleichen). Damit lassen sich harte Kanten vermeiden und Gelenkbereiche wie Ellbogen oder Knie sauber verformen.

### Einfügen in Unreal
Für den Export ist ein konsistentes Rig wichtig: gleiche Ausrichtung, klare Root-Struktur und einheitliche Benennung. In Unreal werden Armature und Animationen als FBX importiert. Entscheidend ist, dass die Animationen im selben Skeleton bleiben, damit sie austauschbar und wiederverwendbar sind. So kann z. B. eine Geh-Animation an mehreren Figuren genutzt werden, solange das Skelett kompatibel bleibt.

## Game Sound

Game Sound ist weit mehr als akustische Dekoration. Im Computerspiel übernimmt er eine doppelte Funktion: Einerseits erhöht er die Immersion, indem er die künstliche Spielwelt mit glaubwürdigen Klangräumen füllt, andererseits liefert er dem Spieler unmittelbares Feedback auf Handlungen, Ereignisse und Zustandswechsel. Fehlen Hintergrundgeräusche, wirkt eine Szene schnell künstlich und leer; sind sie stimmig gestaltet, werden sie oft kaum bewusst wahrgenommen, stabilisieren aber das Erleben der Spielwelt nachhaltig.

Im Unterschied zu linearen Medien entsteht Sound im Spielkontext unter interaktiven Bedingungen. Atmo, Musik, Sprache und Geräusche werden nicht in einer fixen Reihenfolge abgespielt, sondern können sich abhängig von Spieleraktionen zeitlich unvorhersehbar überlagern. Genau daraus ergeben sich zentrale gestalterische Herausforderungen: Sprachverständlichkeit muss erhalten bleiben, klangliche Konflikte zwischen Ebenen sollen vermieden werden, und trotzdem muss ein konsistenter Gesamteindruck entstehen. Eine strukturierte Klanghierarchie und ein bewusstes Lautstärke- und Mischungsverhältnis sind daher Grundvoraussetzungen für professionellen Gamesound.

### Musikpsycholigische Grundlagen
#### Wahrnehmung von Tönen
Die Wahrnehmung von Tönen wird in der musikpsychologischen Lehre von Ernst Kurth als Erleben von „Strebewirkungen“ beschrieben: Töne und Intervalle wirken nicht statisch, sondern erzeugen den Eindruck von gerichteter Bewegung, Spannung und möglicher Auflösung. Die Strebetendenz-Theorie (Willimek) erweitert diesen Ansatz, indem sie diese Wirkung als psychologische Identifikation des Hörers mit Willensregungen deutet. Vereinfacht bedeutet das: Der Hörer erlebt nicht nur eine Klangbewegung, sondern einen inneren Impuls gegen oder für eine Veränderung.

> „Wir erleben einen Ton nicht als Frequenz, sondern als undefinierbares Ding, das wir jedoch nicht als sinnvoll in unsere materielle Welt eingegliedert erfahren können.“ (Musik und Emotionen, S. 3)

Diese Sichtweise verdeutlicht, dass Töne nicht nur als messbare physikalische Signale verarbeitet werden, sondern als psychisch bedeutungsvolle Klangereignisse.

Für Leitton- und Vorhaltswirkungen wird dieses Prinzip konkret über Spannung erklärt. Dissonante Reibungen (z. B. Sekundreibungen im Obertonbereich) werden teilweise unbewusst wahrgenommen und erzeugen ein Spannungsfeld, das eine Auflösung erwartet. Daraus entsteht der typische Eindruck von Erwartung und Zielgerichtetheit in musikalischen Verläufen. Für den Gamesound ist dieser Mechanismus zentral, weil er genutzt werden kann, um Aufmerksamkeit zu lenken, Unsicherheit zu steigern und Auflösungsmomente dramaturgisch wirksam zu setzen.

#### Basisemotionen
Im Kontext von Musik und Emotionen werden Basisemotionen nicht isoliert betrachtet, sondern als Ergebnis mehrerer Parameter, vor allem Harmonik, Tempo und Lautstärke. In den dargestellten Testansätzen wurden Musikbeispiele bewusst auf wenige Parameter reduziert, um den emotionalen Kern sichtbar zu machen. Dabei zeigt sich: Das Zusammenspiel aus harmonischer Struktur und zeitlicher/klanglicher Gestaltung bestimmt maßgeblich die wahrgenommene Emotion.

Eine besondere Rolle spielt das Tempo. Schnellere Verläufe erhöhen typischerweise Aktivierung und werden häufiger mit Erregung, Anspannung oder Durchsetzungskraft verbunden, während langsamere Verläufe eher Ruhe, Trauer oder Gelöstheit stützen. Zusätzlich zeigen physiologische Befunde, dass aktivierende Musik mit erhöhter Herzfrequenz und Muskelspannung korreliert, beruhigende Musik hingegen mit sinkender Herzfrequenz. Damit wird die emotionale Wirkung nicht nur subjektiv beschrieben, sondern auch körperlich nachvollziehbar.

Typische emotionale Zuordnungen aus den dargestellten Harmoniezusammenhängen sind:
- **Dur-Tonika**: nüchternes Einverstanden-Sein mit dem Gegenwärtigen.
- **Moll-Tonika**: Trauer (bei leiser/langsamer Ausprägung) oder Zorn (bei lauter/schneller Ausprägung).
- **Äolisches Moll**: Mut, Abenteuer, Spannung, Gefahr.
- **Subdominante in Dur**: Freude, Überschwänglichkeit, Feierlichkeit.
- **Verminderter Septakkord / kleine Sexte**: Schrecken, Verzweiflung, Bedrohung, Angst.
- **Übermäßiger Dreiklang**: Staunen, Überraschung, Verwandlung.

Diese Zuordnungen sind für Gamesound praktisch nutzbar, weil sie eine gezielte Kopplung von Spielsituation und musikalischem Ausdruck erlauben (z. B. Gefahrensignal, Triumphmoment, Trauerphase).

#### Mechanismen der Musikemotion
Ein etablierter Erklärungsrahmen für musikalisch ausgelöste Emotionen ist das BRECVEM-Modell nach Juslin & Västfjäll. Es beschreibt sieben unterschiedliche Auslösemechanismen, die parallel oder kombiniert wirken können:

- **B – Brain Stem Reflex**: Plötzliche, laute, dissonante oder sehr schnelle Signale lösen unmittelbare Alarm- bzw. Aktivierungsreaktionen aus.
- **R – Rhythmic Entrainment**: Externe Rhythmen synchronisieren innere Rhythmen (z. B. Herzrate), wodurch Aktivierung und Erregung mitgesteuert werden.
- **E – Evaluative Conditioning**: Musik wird emotional wirksam, weil sie wiederholt mit positiven oder negativen Ereignissen gekoppelt wurde.
- **C – Emotional Contagion**: Hörer übernehmen den wahrgenommenen emotionalen Ausdruck der Musik durch innere Nachbildung.
- **V – Visual Imagery**: Musik erzeugt innere Bilder, die wiederum Emotionen auslösen oder verstärken.
- **E – Episodic Memory**: Musik aktiviert autobiografische Erinnerungen und damit verbundene Gefühle.
- **M – Musical Expectancy**: Erwartungen an den Fortgang der Musik werden erfüllt, verzögert oder verletzt; daraus entstehen Spannung, Überraschung und Auflösung.

Gerade für interaktive Medien ist dieses Modell hilfreich, weil es zeigt, dass Musikemotionen nicht nur über Harmonik entstehen, sondern auch über Konditionierung, Rhythmuskopplung, Erwartungssteuerung und Erinnerungseffekte.

### Interaktive Musik in Videospielen
Interaktive Musik ist im Gamesound kein statischer Hintergrund, sondern ein steuerbares System. Ihre zentrale Aufgabe besteht darin, das Spielgeschehen emotional zu unterstützen, ohne den Spielfluss zu stören. Im Unterschied zur Filmmusik ist der genaue Zeitpunkt von Szenenwechseln oder Gefahrensituationen im Spiel oft nicht vorhersehbar. Dadurch muss Musik so entworfen werden, dass sie flexibel auf Spielerhandlungen reagieren kann und trotzdem musikalisch zusammenhängend bleibt.

#### Adaptive vs. dynamische Musik

Im praktischen Einsatz lassen sich zwei komplementäre Verfahren unterscheiden, die oft kombiniert werden:

**Adaptive Musik** funktioniert zustandsorientiert. Sie wechselt zwischen vordefinierten Musikzuständen (States), die jeweils an eine konkrete Spielsituation gebunden sind. Mit **Musikzuständen** sind klar definierte Spielphasen gemeint, beispielsweise:
- **Erkundung** (ruhig, wenig rhythmische Dichte),
- **Gefahr im Anmarsch** (wachsender Puls/Spannung),
- **Kampf** (hohe Intensität, dichteres Arrangement),
- **Nach dem Kampf** (Reduktion und Entspannung).

Der Wechsel zwischen diesen States wird durch konkrete Spielparameter ausgelöst – etwa Gegnernähe, Alarmstatus, Lebenspunkte, Ortswechsel oder Missionsfortschritt. Die Musik wechselt einmal, wenn der State eintritt, und bleibt dann in diesem Zustand bestehen, bis sich eine neue Spielbedingung ergibt.

**Dynamische Musik** hingegen arbeitet parametrisch und kontinuierlich. Während ein Musikstück läuft, werden einzelne Parameter in Echtzeit angepasst – nicht der State selbst, sondern die Eigenschaften der bereits spielenden Musik. Typische dynamische Parameter sind:
- **Lautstärke:** Erhöhung bei Gegnerannaherung, Reduktion bei Sicherheit,
- **Instrumentierung:** Hinzufügen von aggressiveren Instrumenten oder Entfernung von beruhigenden Pads mit wachsender Gefahr,
- **Rhythmische Dichte:** Das Tempo der Schlagzeug- oder Bassmuster wird schneller/komplexer, je intensiver die Situation wird,
- **Filterung:** Hochpass- oder Tiefpassfilter verändern die Klarheit oder Dunkelheit des Klangs je nach Atmosphäre.

Ein konkretes Beispiel: Ein Boss-Kampf könnte mit einem Musikstück im "Kampf"-State beginnen. Während der Spieler den Boss bekämpft, werden Lautstärke und Rhythmusdichte dynamisch an die verbliebenen Lebenspunkte des Gegners angekoppelt. Sinken diese kritisch ab, könnte ein zusätzlicher Streicher-Swell hinzugefügt werden, ohne den State zu wechseln. Nach dem Kampf erfolgt dann der Umschlag auf den State "Nach dem Kampf".

**Zusammenhang:** Beide Ansätze verfolgen dasselbe Ziel: Die Musik soll den aktuellen Spielzustand hörbar machen. Adaptive Musik bietet große emotionale Sprünge (z. B. von Erkundung zu Kampf), während dynamische Musik feinere Abstufungen ermöglicht. Diese Reaktionsfähigkeit ist entscheidend, weil in interaktiven Medien mehrere Soundebenen (Atmosphäre, Geräusche, Sprache, Musik) gleichzeitig aktiv sein können. Musik muss daher nicht nur emotional passen, sondern sich auch in das Gesamtmixing einordnen, damit etwa Sprachverständlichkeit nicht leidet.

#### Looping-Techniken
Looping ist eine Grundtechnik interaktiver Musik, da Spielsituationen unterschiedlich lange dauern. Musik wird deshalb meist als nahtloser Kreis aufgebaut, damit keine hörbaren Brüche entstehen, wenn ein Abschnitt länger aktiv bleibt.

Für professionelle Übergänge zwischen Zuständen werden laut den beschriebenen Produktionsansätzen vor allem zwei Verfahren genutzt:

- **Überblendung (Crossfade)** zwischen zwei Musikzuständen.
- **Takt- oder phasenbezogener Wechsel**, bei dem der Übergang an musikalisch sinnvollen Punkten erfolgt.

In der Praxis ist die Überblendung robuster, weil sie auch bei unvorhersehbaren Spieleraktionen funktioniert. Taktgenaue Wechsel klingen musikalisch sauberer, benötigen aber ein enger abgestimmtes Musiksystem.

#### Layer-Systeme
Layer-Systeme teilen einen Musikzustand in mehrere Ebenen, die je nach Spielsituation zu- oder abgeschaltet werden. Typische Layer sind z. B. Rhythmus, Harmonie, Flächen oder Percussion-Akzente. Dadurch kann die Musik stufenlos verdichtet werden, ohne dass das Grundthema wechselt.

Der Vorteil liegt in der hohen Kontrolle über Intensität und Dramaturgie:

- Bei ruhigen Phasen laufen nur Basis-Layer.
- Bei steigender Gefahr werden zusätzliche Layer aktiviert.
- Nach einer Entspannung werden Layer wieder reduziert.

Dieses Verfahren passt besonders gut zu den Anforderungen interaktiver Klanggestaltung, weil es musikalische Kontinuität mit klarer Spielrückmeldung kombiniert und Überlagerungen mit Sprache/Atmo besser steuerbar macht.


----

## Praktisch

### Design

Die grundsätzliche Inspiration stammt von den Rittern des Mittelalters. Vor allem in der Rüstungskonstruktion sieht man, wie die Rüstung aufgebaut ist. Es wird vor allem auf eine Kombination aus Kettenrüstung sowie Helm und Brustpanzer mit Arm-/ Beinschienen gesetzt.

Die Kettenrüstung ist jedoch nicht gut geeignet für den Modellierungsstil **Low-Poly**.

#### Low-Poly-Stil

Low-Poly ist ein simpel gehaltener Stil mit relativ wenigen Polygonen (Punkten).  
Der große Vorteil dieses Stils liegt vor allem in der Performance.

Grundsätzlich gilt:
> Je weniger Punkte ein Modell besitzt, desto weniger muss der PC beim Rendern berechnen.

Um zu überprüfen, wie viele Punkte ein Modell besitzt, muss dieses exportiert und anschließend als **FBX-Datei** betrachtet werden. Unter **3dviewer.net** erhält man dafür eine gute Übersicht.

#### Helmgestaltung

Eine weitere unübliche Gestaltung ist der Helm. Untypisch sind dabei vor allem die Hörner sowie generell die auffällige Farbgestaltung. Hörner an Helmen gab es im Mittelalter nur sehr selten. Wahrscheinlich wurden sie damals kaum verwendet, da sie im Kampf eher hinderlich waren.

#### Farbwahl

Die Farben wurden bewusst gewählt, da diese Funktionen erfüllen sollen.  
Sie unterstützen das Aussehen des Bosses als Oberhaupt des Gegners und tragen zusätzlich eine symbolische Bedeutung.

Die Farbe **Lila** wird beispielsweise häufig mit Macht, Reichtum und Autorität assoziiert. Historisch gesehen war Lila zudem eine Farbe, die sehr schwer herzustellen war und daher auch im Mittelalter als Zeichen von Wohlstand galt.

#### Zeitliche Einordnung der Rüstung

Die Rüstung selbst erinnert eher an das **Hoch- bzw. Spätmittelalter** beziehungsweise an die **Renaissance**, da in diesen Epochen Rüstungen immer kunstvoller gefertigt wurden.

- **Hoch- und Spätmittelalter (ca. 1380–1500)**  
  Diese Epoche bietet sehr guten Rundumschutz am gesamten Körper und eignet sich daher gut für ein Low-Poly-Design.

- **Renaissance**  
  In dieser Zeit wurden Rüstungen sehr detailreich gestaltet, was für Low-Poly-Modelle weniger geeignet ist. Typisch dafür sind stark verzierte Rüstungen oder Elemente wie Kappenhelme und aufwendige Verzierungen.

### Umsetzung mit Blender
#### Modelierung
##### Entwickelte Technicken

Bei längeren Entwicklungen in einem Projekt lehrnt man immer neue Funktionen kennen. Hin und wieder erfindet man auch seine eigene Technicken. In Blender sind es z.B.

- Gegenteil von der Funktion Insert: Wird ausgeführt in dem man eine Fläche extrahiert ohne eine Höhe hinzu zufügen und diese Fläche mit `S` vergrößern. Hier wird vorallem beachtet das keine Flächen überschnitten werden, was bei insert und dann `S` schon der Fall ist.
- Objekte auf einer Kreisbahn verschieben: Verwendet die Technik das man den Ursprung beliebig setzten kann. Nützlich ist das allerdings dann bei Objekten die man auf einen kugelförmigen Objekt bewegen möchte. Da setzt man den Ursprung auf den gleichen wie bei der Kugel und mit `R` bewegt man das Objekt immer im gleichen Abstand bzw. in der gleichen Neigung zur Kugel. Siehe Abbildung

![Objekte auf einer KUgel [@blender]](img/schmiedpeter/kugel_bewegen.png){width=50%}

- Zuerst per Anmerkung vorgezeichnet und dann in der 2d Ansicht bearbeitet, das 2 mal. Diese Funktionalität ist ähnlich zum UV Mapping nur viel simpler.

##### Angehensweiße

Das Design ist schon mal grob festgelegt und es muss eine Strategie heraus gefunden werden wie dieser umgesetzt wird. Sollte man oben anfangen bei den Gleidmassen oder bei besonderen Markmale der Figur. Wegen der besonderen Form weil es üblich ist, wird oben beim Kopf angefangen und geht weiter hinunter und die Gliedmassen sind am Schluss zu Fertigen. Eingeteil wird im Endeffekt so: Helm und Kopf dann zum Körper, der Hals (die Verbindung) wird erst als drittes gemacht, dann Beine und Arme und am Schluss Füße und Hände.

Die Modellierung des Bosses erfolgte nach dem Prinzip, von oben nach unten zu arbeiten, wobei die Gliedmaßen bewusst erst am Ende ausgearbeitet wurden. Diese Vorgehensweise erleichterte es, zunächst die grundlegenden Proportionen und die visuelle Wirkung der Figur festzulegen, bevor Details ergänzt wurden. Der Fokus lag dabei auf einer klaren Silhouette und einer gut erkennbaren Formensprache, die bereits aus der Distanz die Rolle des Bossgegners vermittelt.

###### Helm

Die Kopfform des Helms wurde bewusst höher als rund gestaltet und orientiert sich eher an einer quaderartigen Grundform. Dadurch wirkt der Kopf massiver und dominanter, was die bedrohliche Erscheinung des Bosses zusätzlich verstärkt. Die Gesichtsform weist einen klaren, basalen Schnitt auf, der gezielt hervorgehoben wurde. Das Visier wurde leuchtend gestaltet, um einen mysteriösen und leicht übernatürlichen Eindruck zu erzeugen.

Ein weiteres markantes Merkmal des Helms sind die Hörner. Diese verlaufen mit ihrer Masse nach hinten, wurden jedoch relativ flach gehalten, um die Gesamtform nicht zu überladen. Während der Modellierung zeigte sich, dass die Spitzen der Hörner zunächst an einer falschen Position lagen. Aus diesem Grund wurden sie im weiteren Verlauf neu ausgerichtet, sodass sie sich harmonisch in die Gesamtform des Helms einfügen und die Silhouette nicht negativ beeinflussen.

###### Körper

Beim Körper wurde eine spezielle Modellierungstechnik eingesetzt, bei der quer verlaufende Akzente genutzt wurden, um die körperlichen Strukturen gezielt hervorzuheben. Der Fokus lag dabei insbesondere auf der Brust- und Bauchmuskulatur sowie auf den Schultern, da diese Bereiche maßgeblich zur kraftvollen und einschüchternden Wirkung des Bosses beitragen. Zusätzlich wurden auch sekundäre Elemente wie der Gürtel in das Modell integriert, um den Gesamteindruck stimmig abzurunden.

Im nächsten Schritt wurde ein Cloth-Fallen angewendet, um der Rüstung ein realistischeres Verhalten zu verleihen. Nach Abschluss dieses Arbeitsschrittes wurden nicht mehr benötigte Körperteile unter der Rüstung entfernt. Diese Entscheidung wurde aus Performancegründen getroffen, da verdeckte Geometrie im finalen Spielmodell keinen visuellen Mehrwert bietet, jedoch unnötig Rechenleistung beansprucht.

Während der Umsetzung traten zwei größere Probleme auf. Zum einen war die Rüstung an den Seiten deutlich dünner als im restlichen Bereich, während sie am Rücken teilweise kaum Tiefe aufwies. Dieses Problem wurde behoben, indem die betroffenen Bereiche mit einer Skalierung angepasst und anschließend sauber zusammengeführt wurden, sodass alle Endpunkte korrekt miteinander verbunden sind. Zum anderen waren einzelne Eckpunkte durch überlagernde Flächen schwer zugänglich. Da eine saubere Bearbeitung dadurch nicht möglich war, wurden die letzten Arbeitsschritte rückgängig gemacht und anschließend erneut korrekt umgesetzt. Ohne Probleme kam das Objekt dann trotzdem nicht, dennnoch war dieser eindeutlich besser.

###### Hals
###### Beine
###### Arme
###### Schuhe
###### Hände


##### Probleme und Lösungen
#### Erweiterte Funktionen
##### Farbenordnung
##### Modul verwendung
##### Erweiterung für Animationen
#### Animationen
##### Umsetzung von Animationen von Unreal
##### eigene Animation
###### T-Pose
###### Gehen
###### Laufen
###### ...
###### Schwierigkeiten und Problem
