# Teilaufgabe Schüler Schmiedpeter
\textauthor{Schmiedpeter}

## 1. Theoretisch

### 1.1 Blender
#### &nbsp; 1.1.1 Einleitung in Blender
##### &nbsp; &nbsp; &nbsp;1.1.1.1 Möglichkeiten
Blender ist ein Programm mit vielen Möglichkeiten. Zum einen kann man mit diesem Programm Modellieren außerdem hat diese eine Zeichenfunktion, sowie einen Python Editor. Schon bestehende Modelle kann man Animationen hinzufügen folgend dazu ist es eine nützliche Weise so Videos zu rendern und schneiden.
##### &nbsp; &nbsp; &nbsp;1.1.1.2 Basics der Modelierung

Aufgebaut ist Blender so: in der Mitte ist ein Koordinatensystem, hier passiert das meiste, links davon sind Werkzeuge. Auf der rechten Seite befinden sich die Objekt Hierache bei den man alle Ordner inkl. Kamera und Licht bzw. auch alle Objekte sieht, sowie im unteren Bereich jegliche Module wie Modifier, Material und Physiks.
![Koordinatensystem [@blender]](img/schmiedpeter/Defaultscreen_blender.png){width=90%}
In der Modellierungsansicht gibt es 3 Modi alle haben eine andere Bedeutung
* Objektmodus ist hauptsächlich für den Umgang mit mehrere Objekten und dem einfügen von Objekten. Vom Programm bereit gestellte Objekte sind der Würfel, Quader, Zylinder, die Kugel und viele mehr. Standard gemäß sind diese auf die Größe 1 Meter gesetzt und am `Set Origin` gesetzt, welches man beides gleich ändern kann. Außerdem wird dieser Modus für Module wie Physiks oder Modifier verwendet.
  Die wichtigsten Werkzeuge sind Objekte bewegen/rotieren/skalieren
* Der Editmodus ist ein wenig anders, dieser ist nämlich da um einzelne Objekte zu verändern
  >  Der Modus funktioniert auch mit meheren Objekten, es ist nur nicht erwünscht weil ungewollte Fehler auftretten können. Aus diesem Grund sollten Objekt vor den ändern  im Editmode gruppieren.
  
	Auswählen funktioniert anders als im Objektmodus hier wählt man nicht ein Objekt aus sondern es hängt ab welche Ansicht ausgewählt ist. Standard ist die Punktansicht ausgewählt, hierbei können nur Ecken angewählt werden. Nach dem gleichen Prinzip funktioniert die Kanten- und Flächenansicht. *Tipp mit `Shift` kann man mehrere auswählen und mit `Str` wählt Blender alle aus, die auf der Bahn zum erst ausgewählten*.
Wichtige Werkzeuge sind Loop Cuts und das Messer (mit diesen beiden fügt mann Kanten hinzu), bewegen, Flächen verkleinern und extrahieren bzw. füllen

* Skulptur Modus 
  
#### &nbsp;1.1.2 Konkurrenz
Neben Blender hätte man sich noch für andere Modellierungsprogramme entscheiden können Beispielsweise *Tinkercad, AutoDesk Fusion oder OpenSCAD*. 
* Tinkercad kennt man vorallem auch durch das Entverwerfen von einfachen Schaltkreisen online und so in etwa ist es bei deren Programm für das Modellieren.
Das Programm ist sehr simple und leicht zu verstehen - Perfekt für Anfänger
Aber nicht geeignet für die Diplomarbeit, weil man extreme Einschränkungen hat. Man kann keine Modelle im Nachhinein abrunden, da Tinkercad nur an vorgefertigte Objekte zum Bewegen hat. Diese Modelle sind fix gefertigt und nicht veränderbar.
* AutoDesk Fusion ist spezialiesiert auf die Produktion bzw. auf Werkzeug und Maschinen. Das heißt aber nicht das dieses Programm nicht geeignet ist für das Modelieren 
AutoDesk hat eine einfacher Handhabung *Zitat aus dem Video*. Aus iesem Grund verwenden dieses Tool sehr viele größere Firmen, wie: Yamaha und Toyota *- so deren Homepage*
Nachteil ist das Programm kostet viel .
* OpenSCAD ist ein Open-Source  Program für das Modellieren per Code. Aus diesem Grund ist dieses Programm nicht geeignet für ein großes Projekt, wegen der hohen Komplexität.



#### &nbsp;1.1.3 Nützliche Befehle

### 1.2 Erweiterte Funktionen in Blender
#### &nbsp; 1.2.1 Material
#### &nbsp; 1.2.2 Module (Modifyers)
##### &nbsp; &nbsp; &nbsp;1.2.2.1 Boolean
##### &nbsp; &nbsp; &nbsp;1.2.2.2 Mirror
##### &nbsp; &nbsp; &nbsp;1.2.2.3 Physiks
#### &nbsp; 1.2.3 Programmieren 
##### &nbsp; &nbsp; &nbsp;1.2.3.1 Nutzen
##### &nbsp; &nbsp; &nbsp;1.2.3.2 Syntax

### 1.3 Animationen
#### &nbsp; 1.3.1 Basics 
#### &nbsp; 1.3.2 Wichtig zu beachten
#### &nbsp;1.3.4 Einfügen in Unreal

## 2. Praktisch
### 2.1 Design
### 2.2 Umsetzung mit Blender
#### &nbsp;2.2.1 Modelierung
#####  &nbsp;&nbsp;2.2.1.1 Entwickelte Technicken
##### &nbsp;&nbsp;2.2.1.2 Angehensweiße
##### &nbsp;&nbsp;2.2.1.3 Probleme und Lösungen
#### &nbsp;2.2.2 Erweiterte Funktionen
##### &nbsp;&nbsp;2.2.2.1 Farbenordnung
##### &nbsp;&nbsp;2.2.2.2 Modul verwendung
##### &nbsp;&nbsp;2.2.2.3 Erweiterung für Animationen
#### &nbsp;2.2.3 Animationen
##### &nbsp;&nbsp;2.2.3.1 Umsetzung von Animationen von Unreal
##### &nbsp;&nbsp;2.2.3.2 eigene Animation
###### &nbsp;&nbsp;&nbsp;2.2.3.2.1 T-Pose
###### &nbsp;&nbsp;&nbsp;2.2.3.2.2 Gehen
###### &nbsp;&nbsp;&nbsp;2.2.3.2.3 Laufen
###### &nbsp;&nbsp;&nbsp;2.2.3.2.4 ...
###### &nbsp;&nbsp;&nbsp;2.2.3.2.5 Schwierigkeiten und Problem


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

