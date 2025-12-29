# Teilaufgabe Peißl
\textauthor{Nevio Peißl}

Dieser Teil der Diplomarbeit beschäftigt sich mit der erstellung des Bossraummodelles und UI sowie der Cutscenes. Hier werden die Designentscheidungen sowie dessen Umsetzung wiedergegeben.

## Literaturrecherche

In diesem Teil werden die theoretischen Aspekte für die Erstellung eines 3D Modelles, UI sowie Cutscenes, welche für "ConquerTheCastle" benötigt werden, behandelt. 

### Blender

Blender ist ein Open-Source-3D-Programm, das von der Blender Foundation entwickelt wird und kostenlos zugänglich ist. Es deckt alle wesentlichen Schritte der 3D-Modellierung ab. Dazu zählen Modeling, Animation, Simulation, Rendering und Exportieren. Dadurch ist es möglich, den gesamten 3D-Workflow innerhalb von Blender durchzuführen, ohne die Verwendung externer Software. [@blender_features]

Die Mission von Blender ist es, ein leistungsstarkes 3D-Programm für jeden frei zugänglich zumachen. Blender wird von der Comunity entwickelt und jeder kann einen Beitrag leisten. 

Blender ist die optimale Lösung für diese Arbeit, da es frei zugänglich, leistungsstark und eine große aktive Comunity hat. Es gibt viele frei zugängliche online Tutorials und Dokumentationen. Die Software bekommt regelmäig Updates und wird ständig erweitert. Blender funktioniert auf den meisten Betriebssystemen (Linux, Windows und MAC) und ist durch OpenGL dynamisch aufgebaut. [@blender_manual]

#### Koordinatensystem

Wenn ein neues Blender Projekt erstellt wird sieht man nur das Koordinatenystem. Es besteht aus drei Achsen: x,y und z. Diese Achsen strecken sich jeweils vom positiven berreich (zb. x positiv) bis hin zum negativen Berreich (zb. x neagtiv) und treffen sich am Nullpunkt. Die Achsen sind gut erkennbar und bietem dem Nutzer einen Fixpunkt, an dem er sich orentieren kann. Außerdem gibt es rechts oben ein kleines Diagramm, welches die Orentierung des Nutzers nochmal in Echtzeit anzeigt. (Siehe Abb. 1) [@blender_manual]


![Koordinatensystem [@blender]](img/peissl/koordinatensystem.png){width=90%}

Die Kamera des Benutzers kann mit `mouse wheel` rotiert und mit `shift + mouse wheel` bewegt werden. [@blender_manual]

Der 3D Cursor, welcher in der Mitte von Abb. 1 zusehen ist, ist der Ort, wo neue Objekte hinzugefügt werden. Dieser Cursor ist standartmäßig am Nullpunkt und kann frei mit `shift + right mouse button` im 3D Raum verschoben werden. Wenn er verschoben wird, ändert sich die Position, an der in Zukunft Objekte eingefügt werden. Der Cursor kann mit `shift + c` wieder zum Nullpunkt gebracht werden. [@blender_manual]

#### Primitive Objekte

In Blender gibt es einige Basisobjekte, welche mithilfe der Tastenkombintion `shift + a` eingefügt werden können. Darunter zählen unter anderem der Würfel, der Zylinder oder der Ball. (Siehe Abb. 2) Diese Objekte haben typische Anwendungsfälle. Wenn ein Gebäude erstellt werden soll, ist es sinnvoll einen Würfel zu benutzen, wenn eine Säule benötigt wird, kommt der Zylinder zum einsatz. [@blender_manual]

Wenn ein Objekt ausgewählt ist, wird es orange Umrandet. Dieses Objekt kann nun bearbeitet werden und der Ursprung des Objektes wird sichtbar. (Siehe Abb. 2, Zylinder) [@blender_manual]

![Objekte [@blender]](img/peissl/objekte.png){width=90%}


Objekte bestehen aus Faces, Edges und Vertecies. Vertecies sind die kleinste Form eines darstellbaren Objektes in Blender. Ein Vertex ist genau ein Punkt. Wenn zwei Punkte verbunden werden, entsteht eine Kante (Edge). Wenn mehere Edges verbunden werden, erhällt man eine Fläche (Face). Verbinden sich mehere Flächen entsteht ein Mesh, ein Objekt. [@blender_manual]

Diese Onjekte werden verändert, um das gewünschte Ergebnis zu erzielen. Objete können verschoben (`m`), rotiert (`r`) und skaliert (`s`) werden. Wenn ein Objekt verschoben wird und dazu eine Achse (x,y,z) ausgewählt wird, verschiebt sich das Objekt nur auf dieser Achse. Wenn ein Objekt genau einen Meter nach X positiv verschoben werden sollte, lautet der Befehl `g + x + 1`. [@blender_manual]

#### Bearbeitungsmodi

#### Object Mode

Object Mode ist der Standartmodus in Blender. Darin kann man Objekte einfügen, gruppieren, verschieben, skalieren und rotieren. Der Object Mode wird zum Anordnen von Objekten benutzt. Die Geometrie der Objekte kann dabei nicht bearbeitet werden. Der Object Mode ist wichtig, um den Überblick über die gesamte Szene nicht zu verlieren. [@blender_manual]

#### Edit Mode

Im Edit Mode bearbeitet man die geometrie einzelner Objekte. Um in den Edit Mode zu kommen muss man das Objekt auswählen und `tab` drücken. Ein weiteres `tab` und man gelangt wieder im Object Mode. Wichtige Edit Mode Tools sind Extrude `e`, Insert `i`, Loop Cut `ctrl + r`, Bevel `b` und merge vertecies `m`. Mit den Tasten `1`, `2`, `3` kann man zwischen "select Vertecies", "select Edges" und "select Faces" wechseln. [@blender_manual]

#### Mirror
Der Mirror Modifier spiegelt ein Objekt entlang einer oder meheren Achsen. Das Objekt wird über seinen Ursprung gespiegelt. Ein Objekt zu spiegeln reduziert den Aufwand bei symetrischen Modellen erhablich und stellt sicher, dass beide Seiten exakt gleich sind. [@blender_manual]

#### Solidify
Solidify gibt Objekten eine Dicke. Die einfachste Version davon funktioniert ähnlich wie Extrude im Edit Mode. Die Dicke kann man im Modifiers Tab unter "Thickness" einstellen. Man kann das Entresultat mit weitern Einstellungen noch weiter verändern. Die "Even Thickness" Einstellung hällt die Dicke an allen Kanten gleich. "Fill Rim" schließt alle offenen Kanten und verhindert Hohlräume. [@blender_manual]


#### Extra Mesh Objects

Extra Mesh Objects ist ein Add-On für Blender und verfügt über den "Wall Builder". Dieser ermöglicht es, komplexe Wände mit Ziegelsteindesign einfach zu erstellen und bearbeiten. Dieses Add-on ermöglicht es, komplexe Strukturen wie Wände dynamisch generieren zu lassen. (Siehe Abb. 3) [@blender_extra_mesh_objects]

![Wall Builder [@blender]](img/peissl/wallbuilder.png){width=90%}



#### UV-Mapping

UV_Mapping wird zum Texturieren von Objekten benötigt. Es ist der Prozess, wo eine 3D Grafik auf eine 2D Fläche projeziert wird. Das Objekt wird aufgeschnitten und auf eine 2D Textur gelegt. Jede Fläche (Face) bekommt koordinaten auf einer 2D Textur. Wenn diese Textur bearbeitet wird verändert sich auch das Aussehen des Objektes. Ohne UV-Mapping wäre Texturen verzährt und Details gehen verloren. [@uv_mapping_guide] [@gpt_uv_mapping]

![UV Mapping [@uv_mapping_guide]](img/peissl/uv-mapping.png){width=90%}


#### Low-Poly-Moddelierung

Durch die geringe Anzahl von Polygonen bleibt der Rechenaufwand eher gering und die Framerate ist stabiler. Außerdem verkürzen sich Ladezeiten, besonders auf älteren Geräten. Low-Poly hällt den Style einheitlich und reduziert den modellierungs Aufwand drastisch. Ein Low-Poly Spiel setzt nicht auf hochauflösende Grafik oder komplexe Modelle, sondern auf die Einfachkeit und die Effizienz. [@low_poly] [@why_low_poly]

![Low-Poly Beispiel [@low_poly_example]](img/peissl/low-poly-example.png){width=90%}

#### Exportformat

Blender verfügt über das Exportformat FBX, welches zum Datenaustausch zwischen verschiedenen Programmen benötigt wird. FBX ist weitverbreitet und wird von Unreal Engine sovie von vielen anderen unterstützt. Dieses Exportformat ist auf schnellen Export und Speichereffizient optimiert und hat viele nützliche Exportfunktionen. [@blender_manual]




### Unreal Engine

Unreal Engine ist eine leistungsstarke, kostenlose 3D Entwicklungssoftware, die vielseiteig eingesetzt werden kann. Egal ob Spiele programieren, Filme produzieren oder animieren. Unreal verfügt über die gleichen Technologien wie AAA-Gamestudios, nutzbar von jedem. Mit Unreal Engine ist (fast) jeder Entwicklungsschritt in einem einheitlichen Ökosystem, was den Entwicklungsprozess deutlich vereinfacht und es möglich selbst als kleines Entwicklerteam hochwertige Spiele zu entwickeln. [@what_is_unreal_engine] [@unreal_engine_indie]

#### GUI

Das Graphical User Interface, auch Benutzeroberfläche genannt, ist eines der wichtigsten Bestandteile eines Spiels. Unter GUI versteht man alles was vor dem eigentlichen Spiel angezeigt wird. Daruner zählt man alle Menüs und alle Lebens sowie andere Statistikanzeigen. Es wird benötigt, um dem User die nötigen Informationen zugeben. Das GUI dient als Schnittstelle zwischen User und Spiel. Eine Benutzeroberfläche soll einfach, effizient und intuitiv sein. Es ist wichtig dass jedes Element einen Namen hat, der die Funktion des Elementes intuituiv beschreibt. Mithilfe von Farben kann man den Benutzer auf bestimmte Elemente aufmerksam machen und dessen Erfahrung verbessern. Außerdem sollte jede Funktion inerhalb weniger Klicks zu erreichen sein. Funktionen, welche häufiger verwendet werden sollen leicht erreichbar sein. Das GUI muss eine Balance zwischen Funktionen und Design sein. [@ui_guide] [@what_is_a_good_ui]

#### Cutscenes

Eine Cutscene, auch genannt Zwischensequenz, ist eine kurze Filmsequenz in einem Videospiel, welche die Geschichte weiter erzählt. Der Spieler kann während dieser Cutscene nicht eingreifen, er ist der Zuschauer. In UE wird die Cutscene mithilfe des Level Sequenzers erstellt. Zu diesem Sequenzer wird eine Kamera hinzugefügt und in der Timeline wird mithilfe von Keyframes die Kameraposition zu bestimmten Zeitpunkten angegeben. Mit einem Blueprint angegeben, wann die Cutscene aufgerufen wird. [@cutscene_explanation] [@cutscene_tutorial]

\newpage


## Praktische Arbeit

### Modellierung

#### Bossraum
##### Erstellung
##### Designentscheidungen
##### Moddelieren
##### Texturieren
##### Exportieren

#### Items
##### Welche Items werden benötig und warum
##### Moddelieren
##### Texturieren
##### Exportieren

### Unreal Engine
#### Modelle Importieren & Einbauen
#### Texturen hinzufügen

#### GUI erstellen

#### Cutscenes erstellen


halt alles machen idk


> Hier beschreiben Sie ihren praktischen Teil. Es geht darum seine Implementierung / Versuche so darzustellen dass anhand dieser dre Leser erkennen kann was sie wie gemacht haben.

Die Frage nach der Detailgenauigkeit lässt sich wie folgt beantworten: So, dass man Ihre Aufgabenstellung vollständig  nachvollziehen kann wenn man nur diese Diplomarbeit in Händen hat!

### Messergebnisse

![Ein PNG Bild\label{fig:png_bild}](img/graph.png){width=70%} 

Bilder sind so scharf wie möglich darzustellen. Unnötige Dinge (welche für den Leser keine Information liefern) sind wegzuschneiden. Üblicherweise versucht das Framework Bilder möglichst gut und vollflächig in die Seite einzupassen - was aber speziell bei kleinen Bildern keinen Sinn macht. Daher kann man die Breite des Bildes `{width=xx%}` beeinflussen. Generell macht es keinen Sinn reisen Bilder mit dieser Funktion niederzuskalieren, sondern eher die Bilder schon vorher mittels eines Bildbearbeitungsprogrammes niederzurechnen. Damit wird das endgültige PDF nicht so groß.

Now a hierarchical tree from this repo:

\dirtree{%
.1 ./.
.2 example.
.3 ....
.2 style.
.3 ....
.2 tools.
.3 docker.
.3 github.
.2 Jenkinsfile.
.2 Makefile.
.2 REAMDE.md.
}


### So gehen Zitate

Hier ein einzel Zitat eines Buches das auf der Seite 17 zu finden ist:  
([@hattie_lernen_2013] S. 17) 

Zitatsammlung:  
(vergleich dazu @heise oder @t3n)  
[@hattie_lernen_2013, S. 33-35; außerdem @leeb_einfuhrung_2016, S. 6 f.]

Zitat ohne Autor  
Hattie sagte bla bla [-@hattie_lernen_2013]

Name des Autors mit Jahr in Klammern  
@hattie_lernen_2013 sagte einmal bla bla bla

Auch Videos kann man Zitieren wi Zum Biespiel hier [@Zatko15] in dieser Referenz.

Hier noch ein Zitat mit Seitenangabe [[@Zatko15] Seite 5f.]

Man darf auch ChatGPT oder andere KIs befragen um Wissen zu erlangen. Dazu muss allerdings ein PDF Log des exakten Chats in die Metadata.yaml eingetragen werden und der dort eingetragene `short-prompt` auch in der bib Datei eingefügt werden. Dann könnten indirekte Zitate so aussehen [@gpt-pandoc] oder auch so [@gpt-atomaufbau].

Wichtig ist es, das beim Author die verwendete KI eingetragen wird (mit Versionsnummern - so genau wie möglich), beim title eine kurze Referenz zum Prompt und beim Jahr - das Jahr in dem die Abfrage gemacht wurde. Das hat dem `short-prompt` aus der metadata.yaml zu entsprechen.

~~~~~
@unpublished{gpt-pandoc,
  author = {{ChatGPT 4.0}},
  title  = {Was ist Pandoc ?},
  year   = {2024},
  url={https://chat.openai.com/c/ef535195-0e39-4d5c-9c85-cdb7ec18ad03},
  urldate = {2023-02-29}
}
~~~~~ 

Oben sieht man wie ein korrekter Bibtech Eintrag für eine ChatGPT Konversation aussieht. Zusätzlich wurden hier bei URL noch die url des Chats eingetragen - was zwar praktisch ist, uns allerdings nicht von der Pflicht entbindet den Chatverlauf in der DA als PDF einzufügen.
Anzumerkein ist ebenfalls noch das wir hier ein `unpublished` Tag verwenden weil wir hier eben Quellen verwenden die in dieser Form nicht gepublished wurden.

### Systembeschreibung Y 

### Systembeschreibung Z 




