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

* Objektmodus ist hauptsächlich für den Umgang mit mehrere Objekten und dem einfügen von Objekten. Vom Programm bereit gestellte Objekte sind der Würfel, Quader, Zylinder, die Kugel und viele mehr. Standard gemäß sind diese auf die Größe 1 Meter gesetzt und am `Set Origin` gesetzt, welches man beides gleich ändern kann. Außerdem wird dieser Modus für Module wie Physiks oder Modifier verwendet.
  Die wichtigsten Werkzeuge sind Objekte bewegen/rotieren/skalieren
  
* Der Editmodus ist ein wenig anders, dieser ist nämlich da um einzelne Objekte zu verändern

   >  Der Modus funktioniert auch mit meheren Objekten, es ist nur nicht erwünscht weil ungewollte Fehler auftretten können. Aus diesem Grund sollten Objekt vor den ändern  im Editmode gruppieren.


	Auswählen funktioniert anders als im Objektmodus hier wählt man nicht ein Objekt aus sondern es hängt ab welche Ansicht ausgewählt ist. Standard ist die Punktansicht ausgewählt, hierbei können nur Ecken angewählt werden. Nach dem gleichen Prinzip funktioniert die Kanten- und Flächenansicht. *Tipp mit `Shift` kann man mehrere auswählen und mit `Str` wählt Blender alle aus, die auf der Bahn zum erst ausgewählten*.
Wichtige Werkzeuge sind Loop Cuts und das Messer (mit diesen beiden fügt mann Kanten hinzu), bewegen, Flächen verkleinern und extrahieren bzw. füllen

* Skulptur Modus verwendet Werkzeuge, die Polys in verschiedene Art und Weisen bewegen. Das einzige Problem dabei ist, das die Polys die bewegt wurden nicht nach genauen Massen bewegt werden können. Außerdem ist zu achten, dass das Objekt mehr Polys haben soll, ansonsten wird das Entergebnis nicht den Erwartungen ersprechen.

Als Unterstützung in den jeweiligen Modus existiert dem Tool Anmerkungen. Mit diesem Tool kann man Sachen in der Eigenen Perspektive zeichnen. Im Edit und Objektmodus kann man zusätzlich auch das Tool Messen verwenden. Dieser funktioniert auch wieder in der eigenen Perspektive und ist wie Anmerkungen 2D. 
  
### Konkurrenz

Neben Blender hätte man sich noch für andere Modellierungsprogramme entscheiden können Beispielsweise *Tinkercad, AutoDesk Fusion oder OpenSCAD*. 

* Tinkercad kennt man vorallem auch durch das Entverwerfen von einfachen Schaltkreisen online und so in etwa ist es bei deren Programm für das Modellieren.
Das Programm ist sehr simple und leicht zu verstehen - Perfekt für Anfänger
Aber nicht geeignet für die Diplomarbeit, weil man extreme Einschränkungen hat. Man kann keine Modelle im Nachhinein abrunden, da Tinkercad nur an vorgefertigte Objekte zum Bewegen hat. Diese Modelle sind fix gefertigt und nicht veränderbar.

* AutoDesk Fusion ist spezialiesiert auf die Produktion bzw. auf Werkzeug und Maschinen. Das heißt aber nicht das dieses Programm nicht geeignet ist für das Modelieren 
AutoDesk hat eine einfacher Handhabung *Zitat aus dem Video*. Aus iesem Grund verwenden dieses Tool sehr viele größere Firmen, wie: Yamaha und Toyota *- so deren Homepage*
Nachteil ist das Programm kostet viel .

* OpenSCAD ist ein Open-Source  Program für das Modellieren per Code. Aus diesem Grund ist dieses Programm nicht geeignet für ein großes Projekt, wegen der hohen Komplexität.



### Nützliche Befehle

| Befehl | Nutzen | Weitere erklärung |
|:------:|:------:|:-----------------:|
|   `Shift + A`   |  Objekt hinzufügen    |    / 			  |
|  `X`   |  Löschen   |   Wenn man etwas löschen will kommt eine Bestätigung abfrage			  |
|    `TAB`   |    Wechselt den Modus   |     Von Objekt- auf Editmodus und zurück  		  |
|    `LEERZEICHEN`   |    Zeitleiste abspielen/ stoppen   |  /  |

bei den nächsten Befehle gilt:
e
*  bei zusätzlichen Achsen Tippen `X`/`Y`/`Z` wird diese prioriesiert, mit 2x Tippen unprioriesieren
*  bei `Shift` werden in Blocken bewegt

| Befehl | Nutzen | Weitere erklärung |
|:------:|:------:|:-----------------:|
|    `G`   |    verschieben im Koordinatesystem   |    	/	  |
|    `R`   |    drehen   |    	Um den Ursprung (Oranger Punkt)	  |
|    `S`   |    skalieren   |    	Um den Ursprung 	  |

 Für den Objektmodus

| Befehl | Nutzen | Weitere erklärung |
|:------:|:------:|:-----------------:|
|    `Str + J`   |    Objekte gruppieren   |    Funktioniert bei 2 oder mehr Objekte. Das der Befehl durchgesetzt werden kann, muss ein primär Objekt ausgewählt werden, für z.B	den Ursprung des Objektes |
|    `Rechts Klick` + Ursprung ändern  |    versetzt den Ursprung   |    	Entweder nach Masse, Volumen oder nach dem Set Origin	  |
|    `Rechts Klick` +  Weich schattieren   |    Ecken abrunden   |   ohne Polys hinzufügen |

Für den Editmodus

| Befehl | Nutzen | Weitere erklärung |
|:------:|:------:|:-----------------:|
|    `M`   |    Punkte zusammenfügen   |   Funktioniert bei 2 oder mehr Punkten bzw. auch bei Kanten und Flächen setzen diese aber in Punkte um. Entweder auf dem ersten/ letzten ausgewählten Punkte, in der Mitte oder beim Set Origin. |
|    `Str + R`   |    Loop Cuts   |   Erstellt Kanten die sich um ein ganzes Objekt schlingt. Dazu kann man einstellen wie viele Schleifen erstellt werden |
|    `K`   |    Messer   |   fügt Schnitte zu einen Objekt hinzu. Wird `Shift` gedrückt wird der Schnitt zentral gerichtet|
|    `E`   |    Extrahieren   |   erweitert Flächen bzw. Kanten |
|    `I`   |    Einsetzten von Flächen   |   erzeugt ein kleinere Fläche in einer größeren |
|    `F`   |    Füllen von Flächen und Kanten   |   Bei 2 Punkte wird eine Kante erstellt ansonsten ein Fläche. Bei 5+ Punkte füllen werden oft komische Flächen erzeugt, vor allem für das Rendern und Exportieren ist das wichtig. |
|    `Str + T`   |    Fläche zu Dreieck konventieren |   Trifft zu alle ausgewällten Flächen und ist sinnvoll für das Exportieren bzw. Rendern |


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


### Programmieren 
#### Nutzen
#### Syntax


------

## Animationen
### Basics 
### Wichtig zu beachten
### Einfügen in Unreal

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

* Gegenteil von der Funktion Insert: Wird ausgeführt in dem man eine Fläche extrahiert ohne eine Höhe hinzu zufügen und diese Fläche mit `S` vergrößern. Hier wird vorallem beachtet das keine Flächen überschnitten werden, was bei insert und dann `S` schon der Fall ist.
* Objekte auf einer Kreisbahn verschieben: Verwendet die Technik das man den Ursprung beliebig setzten kann. Nützlich ist das allerdings dann bei Objekten die man auf einen kugelförmigen Objekt bewegen möchte. Da setzt man den Ursprung auf den gleichen wie bei der Kugel und mit `R` bewegt man das Objekt immer im gleichen Abstand bzw. in der gleichen Neigung zur Kugel. Siehe Abbildung

![Objekte auf einer KUgel [@blender]](img/schmiedpeter/kugel_bewegen.png){width=50%}

* Zuerst per Anmerkung vorgezeichnet und dann in der 2d Ansicht bearbeitet, das 2 mal. Diese Funktionalität ist ähnlich zum UV Mapping nur viel simpler.

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
