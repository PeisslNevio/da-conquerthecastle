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

![Koordinatensystem [@blender]](img/schmiedpeter/Material_blender.png){width=90%}

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
### Umsetzung mit Blender
#### Modelierung
##### Entwickelte Technicken

Bei längeren Entwicklungen in einem Projekt lehrnt man immer neue Funktionen kennen. Hin und wieder erfindet man auch seine eigene Technicken. In Blender sind es z.B.

* Gegenteil von der Funktion Insert: Wird ausgeführt in dem man eine Fläche extrahiert ohne eine Höhe hinzu zufügen und diese Fläche mit `S` vergrößern. Hier wird vorallem beachtet das keine Flächen überschnitten werden, was bei insert und dann `S` schon der Fall ist.
* Objekte auf einer Kreisbahn verschieben: Verwendet die Technik das man den Ursprung beliebig setzten kann. Nützlich ist das allerdings dann bei Objekten die man auf einen kugelförmigen Objekt bewegen möchte. Da setzt man den Ursprung auf den gleichen wie bei der Kugel und mit `R` bewegt man das Objekt immer im gleichen Abstand bzw. in der gleichen Neigung zur Kugel. Siehe Abbildung



##### Angehensweiße
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


-------------------

## Theorie

Dieses Kapitel wird oft auch als _Literaturrecherche_ bezeichnet. Da gehört alles rein was der __normale__ Leser braucht um den praktischen Ansatz zu verstehen. Das bedeutet Sie brauchen einen roten Faden !

Das sind z.B: allgemeine Definitionen, Beschreibung von fachspezifischen Vorgehensweisen, Frameworks, Theorie zu verwendeten Algorithmen, besondere Umstände, ...

## Praktische Arbeit

Hier beschreiben Sie ihren praktischen Teil. Es geht darum seine Implementierung / Versuche so darzustellen dass anhand dieser dre Leser erkennen kann was sie wie gemacht haben.

Die Frage nach der Detailgenauigkeit lässt sich wie folgt beantworten: So, dass man Ihre Aufgabenstellung vollständig  nachvollziehen kann wenn man nur diese Diplomarbeit in Händen hat!

### Erzeugen von Java Quellcode

Unter einem Array in Java versteht man ein Feld oder Container, das in der Lage ist, mehrere Objekte vom gleichen Typ aufzunehmen und zu verwalten. Dabei wird in Java das Array als eine spezielle Klasse repräsentiert, was unter anderem mit sich bringt, dass man auf spezielle Methoden und Operationen bei Arrays zurückgreifen kann. Der Umgang mit Arrays mag gerade am Anfang etwas schwerer sein und birgt viele Fehlerquellen, nach und nach wird man das System das hinter den Arrays steht aber gut nachvollziehen können. 

~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~{caption="Initialisieren eines Arrays" .java}
Typ[] Name = new Typ[Anzahl];
Typ Name[] = new Typ[Anzahl];
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Etwas erfahrenere Programmierer werden jetzt schon erkennen, worauf es beim Zugriff auf Elemente im Array meist hinausläuft: Auf Schleifen!
Schleifen sind ein komfortables Mittel um alle Elemente eines Arrays durchzugehen und auf Wunsch auszugeben oder andere Operationen darauf anzuwenden. Allerdings muss man nicht nur hier aufpassen, dass man die länge des Arrays in der Schleife nicht überschreitet und so auf Felder zugreift die gar nicht existieren. Damit so etwas erst gar nicht passiert, kann man in der Abbruchbedingung der for-Schleife direkt die Länge des Arrays ausgeben mit: array.length.

Möchte man nun also alle 5 Elemente unseres Beispiels-Arrays mit einer Schleife ausgeben lassen, dann würde das so gehen:

~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~{caption="Examples of array manipulations" .java}
// (c) by Mike Scott

public class ArrayExamples
{	public static void main(String[] args)
	{	int[] list = {1, 2, 3, 4, 1, 2, 3};
		findAndPrintPairs(list, 5);
		bubblesort(list);
		showList(list);

		list = new int[]{ 1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11};
		bubblesort(list);
		showList(list);

		list = new int[]{11, 10, 9, 8, 7, 6, 5, 4, 3, 2, 1, 0, -1, -2};
		bubblesort(list);
		showList(list);

		list = new int[]{1};
		bubblesort(list);
		showList(list);
	}


	// pre: list != null, list.length > 0
	// post: return index of minimum element of array
	public static int findMin(int[] list)
	{	assert list != null && list.length > 0 : "failed precondition";

		int indexOfMin = 0;
		for(int i = 1; i < list.length; i++)
		{	if(list[i] < list[indexOfMin])
			{	indexOfMin = i;
			}
		}

		return indexOfMin;
	}
}
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Obwohl hier nur java gezeigt ist, unterstützt das Template auch scala, java, javascript, css, html5 und xml

~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~{caption="Ein einfaches XML" .xml}
<?xml version="1.0" standalone="yes"?>
<!DOCTYPE module [
    <!ELEMENT module (module|property|metadata|message)*>
    <!ATTLIST module name NMTOKEN #REQUIRED>
    <!ELEMENT property EMPTY>
    <!ATTLIST property
        name NMTOKEN #REQUIRED
        value CDATA #REQUIRED
        default CDATA #IMPLIED
    >
    <!ELEMENT metadata EMPTY>
    <!ATTLIST metadata
        name NMTOKEN #REQUIRED
        value CDATA #REQUIRED
    >
    <!ELEMENT message EMPTY>
    <!ATTLIST message
        key NMTOKEN #REQUIRED
        value CDATA #REQUIRED
    >
]>

<!--
    Checkstyle configuration that checks if the braces are set correctly
 -->

<module name = "Checker">
    <property name="charset" value="UTF-8"/>
    <property name="severity" value="warning"/>

    <property name="fileExtensions" value="java"/>
    <!-- Checks for whitespace                               -->
    <!-- See http://checkstyle.sf.net/config_whitespace.html -->

    <module name="TreeWalker">
        
        <module name="NeedBraces"/>
        <module name="LeftCurly">
        	<property name="option" value="nl"/>
        </module>

        <module name="RightCurly">
            <property name="id" value="RightCurlyAlone"/>
            <property name="option" value="alone"/>
            <property name="tokens"
             value="CLASS_DEF, METHOD_DEF, CTOR_DEF, LITERAL_FOR, LITERAL_WHILE, STATIC_INIT,
                    INSTANCE_INIT,LITERAL_TRY, LITERAL_CATCH, LITERAL_FINALLY, LITERAL_IF, LITERAL_ELSE,
                    LITERAL_DO"/>
        </module>
    </module>
</module>
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Hier etwas in kotlin

~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~{caption="Ein einfaches Kotlin Beispiel" .kotlin}
// this is a simple code listing:
println("hello kotlin from latex")
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


Und noch ein Beispiel in vba

~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~{caption="Ein einfaches Visual Basic for Applications Beispiel" .vba}
Private Sub ExitSub()
 
    Dim i As Integer
 
    For i = 1 To 10      
        If i = 5 Then
            Exit Sub
            MsgBox "The value of i is" & i
        End If
    Next i 
 
End Sub
 
 
Private Sub CallExitSub()
    Call ExitSub
    MsgBox "Exit Sub"  
End Sub
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


und noch was in Dart (im Markdown direkt als Latex Quellcode eingefügt - damit funktionieren jegliche Sprachen welche als langdef vorliegen) 

\begin{lstlisting}[language=Dart, caption={Ein Beispiel für Dart}]
library hallo;

void main() {
  String x;
  print('Hello, World!');
  x = 'hallo';
}
\end{lstlisting}


### Auswertung der Ergebnisse

Anhand von XY kann man folgende Tabelle ableiten:

| Right | Left | Default | Center |
|------:|:-----|---------|:------:|
|   12  |  12  |    12   |    12  |
|  123  |  123 |   123   |   123  |
|    1  |    1 |     1   |     1  |

: Eine Tolle tabelle

#### Eine Überschrift 4ter Ordnung

Mit etwas Fließtext. Mit etwas Fließtext. Mit etwas Fließtext. Mit etwas Fließtext. Mit etwas Fließtext. Mit etwas Fließtext. Mit etwas Fließtext. Mit etwas Fließtext. Mit etwas Fließtext. Mit etwas Fließtext. Mit etwas Fließtext. Mit etwas Fließtext. Mit etwas Fließtext. Mit etwas Fließtext. Mit etwas Fließtext. Mit etwas Fließtext.


#### Noch ein Überschrift 4ter Ordnung

Mit etwas Fließtext. Mit etwas Fließtext. Mit etwas Fließtext. Mit etwas Fließtext. Mit etwas Fließtext. Mit etwas Fließtext. Mit etwas Fließtext. Mit etwas Fließtext.

Und mit einer Aufzählung:

* Alpha
* Bravo
* Charlie
    * Charlie 1
    * Charlie 2
    * Charlie 3
    * Charlie 4
* Delta
* Epsilon

 Mit etwas Fließtext. Mit etwas Fließtext. Mit etwas Fließtext. Mit etwas Fließtext. Mit etwas Fließtext. Mit etwas Fließtext. Mit etwas Fließtext. Mit etwas Fließtext.

