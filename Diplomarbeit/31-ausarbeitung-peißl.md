# Teilaufgabe Peißl
\textauthor{Nevio Peißl}

Dieser Teil der Diplomarbeit beschäftigt sich mit der Erstellung des Bossraum-Modells, der Benutzeroberfläche (UI) sowie der Cutscenes. Dabei werden die getroffenen Designentscheidungen sowie deren Umsetzung beschrieben.

## Literaturrecherche

In diesem Kapitel werden die theoretischen Grundlagen für die Erstellung von 3D-Modellen, Benutzeroberflächen und Cutscenes, die für das Spiel "ConquerTheCastle" benötigt werden, behandelt.


### Blender

Blender ist ein Open-Source-3D-Programm, das von der Blender Foundation entwickelt wird und kostenlos zugänglich ist. Es deckt alle wesentlichen Schritte der 3D-Modellierung ab. Dazu zählen Modeling, Animation, Simulation, Rendering und Export. Dadurch ist es möglich, den gesamten 3D-Workflow innerhalb von Blender durchzuführen, ohne zusätzliche externe Software zu verwenden. [@blender_features]

Die Mission von Blender ist es, ein leistungsstarkes 3D-Programm für jeden frei zugänglich zu machen. Blender wird von einer großen Community entwickelt, wobei jeder einen Beitrag leisten kann. [@blender_about]

Blender ist für diese Arbeit eine optimale Lösung, da es frei verfügbar, leistungsstark und durch eine große, aktive Community unterstützt wird. Zudem gibt es zahlreiche frei zugängliche Online-Tutorials und umfangreiche Dokumentationen. Die Software erhält regelmäßig Updates und wird kontinuierlich erweitert. Blender ist auf den gängigen Betriebssystemen (Linux, Windows und macOS) verfügbar und basiert auf OpenGL. [@blender_manual]

#### Koordinatensystem

Beim Erstellen eines neuen Blender-Projekts ist zunächst nur das Koordinatensystem sichtbar. Dieses besteht aus drei Achsen: X, Y und Z. Die Achsen erstrecken sich jeweils vom positiven bis zum negativen Bereich und treffen sich im Nullpunkt. Sie dienen als Orientierungshilfe und bieten dem Benutzer einen festen Bezugspunkt innerhalb der Szene. Zusätzlich befindet sich rechts oben ein kleines Achsendiagramm, das die Orientierung des Nutzers in Echtzeit anzeigt (siehe Abb. 1). [@blender_manual]


![Koordinatensystem [@blender]](img/peissl/koordinatensystem.png){width=90%}

Die Kamera kann mit dem Mausrad rotiert und mit Shift + Mausrad verschoben werden. [@blender_manual]

Der 3D-Cursor, der in Abb. 1 sichtbar ist, definiert die Position, an der neue Objekte hinzugefügt werden. Standardmäßig befindet er sich im Nullpunkt und kann mit Shift + rechter Maustaste frei im 3D-Raum verschoben werden. Wird der Cursor versetzt, ändert sich entsprechend die Einfügeposition neuer Objekte. Mit Shift + C kann der Cursor wieder auf den Nullpunkt zurückgesetzt werden. [@blender_manual]

#### Primitive Objekte

Blender bietet mehrere primitive Basisobjekte, die mithilfe der Tastenkombination Shift + A eingefügt werden können. Dazu zählen unter anderem der Würfel, der Zylinder oder die Kugel (siehe Abb. 2). Diese Objekte besitzen typische Anwendungsfälle: Für Gebäude wird häufig ein Würfel verwendet, während sich ein Zylinder besonders für Säulen eignet. [@blender_manual]

Wird ein Objekt ausgewählt, ist es orange umrandet. Der Ursprung des Objekts wird sichtbar, und das Objekt wird im Outliner auf der rechten Seite markiert (siehe Abb. 2, Zylinder). [@blender_manual]

![Objekte [@blender]](img/peissl/objekte.png){width=90%}


Objekte bestehen aus Vertices, Edges und Faces. Ein Vertex stellt einen einzelnen Punkt dar. Werden zwei Vertices verbunden, entsteht eine Edge. Mehrere verbundene Edges ergeben eine Face. Verbinden sich mehrere Faces, entsteht ein Mesh, welches das eigentliche Objekt darstellt. [@blender_manual]

Diese Objekte werden verändert, um das gewünschte Ergebnis zu erzielen. Objekte können verschoben (`G`), rotiert (`R`) und skaliert (`S`) werden. Wenn ein Objekt verschoben wird und dazu eine Achse (X, Y oder Z) ausgewählt wird, verschiebt sich das Objekt nur auf dieser Achse. Wenn ein Objekt genau einen Meter nach X positiv verschoben werden sollte, lautet der Befehl `G + X + 1`. [@blender_manual]

#### Bearbeitungsmodi

##### Object Mode

Der Object Mode ist der Standardmodus in Blender. In diesem Modus können Objekte eingefügt, gruppiert, verschoben, skaliert und rotiert werden. Er dient der Anordnung von Objekten innerhalb der Szene. Die Geometrie der Objekte kann in diesem Modus nicht verändert werden. Der Object Mode ist essenziell, um den Überblick über die gesamte Szene zu behalten. [@blender_manual]

##### Edit Mode

Im Edit Mode bearbeitet man die Geometrie einzelner Objekte. Um in den Edit Mode zu kommen muss man das Objekt auswählen und `Tab` drücken. Ein weiteres `Tab` und man gelangt wieder im Object Mode. Wichtige Edit Mode Tools sind Extrude `E`, Insert `I`, Loop Cut `Ctrl + R`, Bevel `B` und Merge Vertices `M`. Mit den Tasten `1`, `2` und `3` kann zwischen der Auswahl von Vertices, Edges und Faces gewechselt werden. [@blender_manual]

#### Mirror
Der Mirror Modifier spiegelt ein Objekt entlang einer oder mehrerer Achsen, wobei die Spiegelung über den Objektursprung erfolgt. Dieser Modifier reduziert den Arbeitsaufwand bei symmetrischen Modellen erheblich und stellt sicher, dass beide Seiten exakt identisch sind. [@blender_manual]

#### Solidify
Der Solidify Modifier verleiht Objekten eine Dicke. Die einfachste Anwendung ähnelt dem Extrude-Werkzeug im Edit Mode. Die Dicke kann im Modifier-Tab über den Parameter Thickness eingestellt werden. Zusätzliche Optionen ermöglichen eine weitere Anpassung des Ergebnisses. Die Einstellung Even Thickness sorgt für eine gleichmäßige Dicke an allen Kanten, während Fill Rim offene Kanten schließt und Hohlräume verhindert. [@blender_manual]


#### Extra Mesh Objects

Extra Mesh Objects ist ein Add-on für Blender, das die dynamische Erstellung komplexer Strukturen wie Wände ermöglicht. Um es zu nutzen, muss das Add-on installiert sein. Neue Objekte werden über `Shift + A` → Mesh → Extras → Wall Builder erstellt (siehe Abb. 3). [@blender_extra_mesh_objects]

![Wall Builder [@blender]](img/peissl/wallbuilder.png){width=90%}

Es können nun die Eigenschaften dieser Wand bearbeitet werden. Darunter zählen Anfang und Ende der Wand, die Höhe und Breite sowie die Größe der einzelnen Ziegelsteine. Es gibt noch weitere Einstellungen für Fenster, Zinnen und Treppen. [@blender_extra_mesh_objects]




#### UV-Mapping

UV-Mapping wird zum Texturieren von Objekten benötigt. Es ist der Prozess, bei dem eine 3D-Grafik auf eine 2D-Fläche projiziert wird. Das Objekt wird aufgeschnitten und auf eine 2D Textur gelegt. Jede Fläche (Face) bekommt Koordinaten auf einer 2D-Textur. Wenn diese Textur bearbeitet wird, verändert sich auch das Aussehen des Objektes. Ohne UV-Mapping wären Texturen verzerrt, und Details gehen verloren. [@uv_mapping_guide] [@gpt_uv_mapping]

![UV Mapping [@uv_mapping_guide]](img/peissl/uv-mapping.png){width=90%}


#### Low-Poly-Modellierung

Durch die geringe Anzahl von Polygonen bleibt der Rechenaufwand eher gering und die Framerate ist stabiler. Außerdem verkürzen sich Ladezeiten, besonders auf älteren Geräten. Low-Poly hält den Style einheitlich und reduziert den Modellierungsaufwand drastisch. Ein Low-Poly Spiel setzt nicht auf hochauflösende Grafik oder komplexe Modelle, sondern auf die Einfachheit und Effizienz. [@low_poly] [@why_low_poly]

![Low-Poly Beispiel [@low_poly_example]](img/peissl/low-poly-example.png){width=90%}

#### Exportformat

Blender unterstützt das Exportformat FBX, welches zum Datenaustausch zwischen verschiedenen Programmen benötigt wird. FBX ist weit verbreitet und wird von Unreal Engine sowie von vielen anderen unterstützt. Dieses Exportformat ist auf schnellen Export und Speichereffizienz optimiert und hat viele nützliche Exportfunktionen. [@blender_manual]




### Unreal Engine

Die Unreal Engine (im Folgenden UE genannt) ist eine leistungsstarke, kostenlose 3D-Entwicklungssoftware, die vielseitig eingesetzt werden kann. Egal ob Spiele programmieren, Filme produzieren oder animieren. UE verfügt über die gleichen Technologien wie AAA-Gamestudios und ist für jeden nutzbar. Mit Unreal Engine ist (fast) jeder Entwicklungsschritt in einem einheitlichen Ökosystem integriert, was den Entwicklungsprozess deutlich vereinfacht und es ermöglicht, selbst als kleines Entwicklerteam hochwertige Spiele zu entwickeln. [@what_is_unreal_engine] [@unreal_engine_indie]

#### GUI

Das Graphical User Interface (GUI), auch Benutzeroberfläche genannt, ist eines der wichtigsten Bestandteile eines Spiels. Unter GUI versteht man alles, was vor dem eigentlichen Spiel angezeigt wird. Darunter zählt man alle Menüs sowie Lebens- und andere Statistikanzeigen. Es wird benötigt, um dem User die nötigen Informationen zu geben. Das GUI dient als Schnittstelle zwischen User und Spiel. Eine Benutzeroberfläche soll einfach, effizient und intuitiv sein. Es ist wichtig, dass jedes Element einen Namen hat, der die Funktion des Elementes intuitiv beschreibt. Mithilfe von Farben kann man den Benutzer auf bestimmte Elemente aufmerksam machen und dessen Erfahrung verbessern. Außerdem sollte jede Funktion innerhalb weniger Klicks zu erreichen sein. Funktionen, welche häufiger verwendet werden sollen leicht erreichbar sein. Das GUI muss eine Balance zwischen Funktionen und Design sein. [@ui_guide] [@what_is_a_good_ui]

Die GUI wird in Unreal Engine mithilfe von UMG (Unreal Motion Graphics) erstellt. Dazu erstellt man Widgets und bindet diese in das Spiel ein. Diese Widgets werden mit dem HUD (Heads Up Display) angezeigt und der Blueprint im Hintergrund steuert das Verhalten des Widgets. Dazu gibt es einen eigenen UMG-Editor in UE, der alle notwendigen Funktionen an einem Platz bündelt. [@ui_tutorial]

#### Cutscenes

Eine Cutscene, auch genannt Zwischensequenz, ist eine kurze Filmsequenz in einem Videospiel, welche die Geschichte weiter erzählt. Der Spieler kann während dieser Cutscene nicht eingreifen, er ist der Zuschauer. [@cutscene_explanation]

In UE wird die Cutscene mithilfe des Level Sequenzers erstellt. Zu diesem Sequenzer wird eine Kamera hinzugefügt und in der Timeline wird mithilfe von Keyframes die Kameraposition zu bestimmten Zeitpunkten angegeben. Mithilfe eines Blueprints wird festgelegt, wann die Cutscene aufgerufen wird.  [@cutscene_tutorial]

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
##### Modellieren
##### Texturieren
##### Exportieren

### Unreal Engine
#### Modelle Importieren & Einbauen
#### Texturen hinzufügen

#### GUI erstellen

#### Cutscenes erstellen


