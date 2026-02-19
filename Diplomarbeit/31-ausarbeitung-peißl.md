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


![Koordinatensystem [@blender]](img/peissl/theorie/koordinatensystem.png){width=90%}

Die Kamera kann mit dem Mausrad rotiert und mit Shift + Mausrad verschoben werden. [@blender_manual]

Der 3D-Cursor, der in Abb. 1 sichtbar ist, definiert die Position, an der neue Objekte hinzugefügt werden. Standardmäßig befindet er sich im Nullpunkt und kann mit Shift + rechter Maustaste frei im 3D-Raum verschoben werden. Wird der Cursor versetzt, ändert sich entsprechend die Einfügeposition neuer Objekte. Mit Shift + C kann der Cursor wieder auf den Nullpunkt zurückgesetzt werden. [@blender_manual]

#### Primitive Objekte

Blender bietet mehrere primitive Basisobjekte, die mithilfe der Tastenkombination Shift + A eingefügt werden können. Dazu zählen unter anderem der Würfel, der Zylinder oder die Kugel (siehe Abb. 2). Diese Objekte besitzen typische Anwendungsfälle: Für Gebäude wird häufig ein Würfel verwendet, während sich ein Zylinder besonders für Säulen eignet. [@blender_manual]

Wird ein Objekt ausgewählt, ist es orange umrandet. Der Ursprung des Objekts wird sichtbar, und das Objekt wird im Outliner auf der rechten Seite markiert (siehe Abb. 2, Zylinder). [@blender_manual]

![Objekte [@blender]](img/peissl/theorie/objekte.png){width=90%}


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

Extra Mesh Objects ist ein Add-on für Blender, das die dynamische Erstellung komplexer Strukturen wie Wände ermöglicht. Um es zu nutzen, muss das Add-on installiert sein. Neue Wall Objekte werden mit `Shift + A` und dem Wall Builder erstellt (siehe Abb. 3). [@blender_extra_mesh_objects]

![Wall Builder [@blender]](img/peissl/theorie/wallbuilder.png){width=90%}

Es können nun die Eigenschaften dieser Wand bearbeitet werden. Darunter zählen Anfang und Ende der Wand, die Höhe und Breite sowie die Größe der einzelnen Ziegelsteine. Es gibt noch weitere Einstellungen für Fenster, Zinnen und Treppen. [@blender_extra_mesh_objects]




#### UV-Mapping

UV-Mapping wird zum Texturieren von Objekten benötigt. Es ist der Prozess, bei dem eine 3D-Grafik auf eine 2D-Fläche projiziert wird. Das Objekt wird aufgeschnitten und auf eine 2D Textur gelegt. Jede Fläche (Face) bekommt Koordinaten auf einer 2D-Textur. Wenn diese Textur bearbeitet wird, verändert sich auch das Aussehen des Objektes. Ohne UV-Mapping wären Texturen verzerrt, und Details gehen verloren. [@uv_mapping_guide] [@gpt_uv_mapping]

![UV Mapping [@uv_mapping_guide]](img/peissl/theorie/uv-mapping.png){width=90%}


#### Low-Poly-Modellierung

Durch die geringe Anzahl von Polygonen bleibt der Rechenaufwand eher gering und die Framerate ist stabiler. Außerdem verkürzen sich Ladezeiten, besonders auf älteren Geräten. Low-Poly hält den Style einheitlich und reduziert den Modellierungsaufwand drastisch. Ein Low-Poly Spiel setzt nicht auf hochauflösende Grafik oder komplexe Modelle, sondern auf die Einfachheit und Effizienz. [@low_poly] [@why_low_poly]

![Low-Poly Beispiel [@low_poly_example]](img/peissl/theorie/low-poly-example.png){width=90%}

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

In diesem Kapitel wird die praktische Umsetzung des Bossraums, der Items, der GUI und der Cutscenes beschrieben.

### Bossraum

Der Bossraum ist der zentrale Schauplatz des Spiels. Dieser Raum erinnert an einen Thronsaal und bietet ausreichend Platz für den Kampf. Wenn der Spieler den Bossraum betritt, soll er das Gefühl haben, vor einem entscheidenden Kampf zu stehen.
#### Konzept

Das Konzept des Bossraums orientiert sich an mittelalterlichen Thronsälen. Der Raum ist länglich aufgebaut und führt den Spieler vom Eingangsbereich direkt bis zum Thron des Bosses. Elemente wie Säulen, hohe Decken, Fenster und Banner wurden verwendet, um die Macht des Bosses widerzuspiegeln.
Der Spieler kann sich während des Kampfes leicht orientieren, da der Bossraum übersichtlich aufgebaut ist und jedes Objekt, das sich darin befindet, einen klaren Nutzen hat.

Nachfolgend ist die Skizze des Bossraums dargestellt. In der Skizze sind die Eingangstür (links), der rote Teppich (orange), die Säulen (grün) und der Thron (rot) eingezeichnet. Außerdem ist die Position der Fenster violett gekennzeichnet. Der Bossraum hat eine Länge von 70 Metern, eine Breite von 30 Metern und eine Höhe von 20 Metern.

![Bossraum Konzept](img/peissl/praxis/konzept-bossraum.jpg){width=90%}

#### Modellierung

Die Modellierung des Bossraumes wurde vollständig im 3D-Modellierungsprogramm Blender durchgeführt. Das Modellierungsverfahren erfolgte in mehreren iterativen Schritten: Zunächst wurden die Grundstrukturen des Bodens und der Wandflächen grob modelliert, um die räumliche Grundform zu etablieren. Die Wandkonstruktion wurde unter Verwendung des Blender-Add-ons „Wall Builder" erstellt, um eine effiziente und realistische Modellierung zu ermöglichen. 

Anschließend wurden die tragenden Säulen sowie der Thronsessel als zentrale Designelemente integriert. Der Thronsessel wurde bewusst auf einer erhöhten Plattform positioniert, die durch eine Treppe erreichbar ist. Diese Designentscheidung verfolgt das Ziel, der Boss-Figur eine visuelle Hierarchie und eine übergeordnete Positionierung gegenüber dem Spieler zu verleihen. Die Fensterpositionierung wurde strategisch so gewählt, dass stets mindestens eine Säule zwischen benachbarten Fenstern positioniert ist, um Sichtblockaden zu erzeugen.

Für die Eingangstür wurde eine Öffnung aus der Wandfläche geschnitten, um eine authentische Türöffnung zu schaffen und dem Spieler eine intuitive räumliche Wahrnehmung zu ermöglichen. Für die Raumdecke wurde ein Gewölbesystem gewählt, da es die Blickrichtung des Spielers gezielt auf die zentrale Boss-Position lenkt und damit die Spielmechanik unterstützt. Das Gewölbesystem wird durch mehrere kleinere, stützende Gewölbe strukturiert, die die Deckenarchitektur mit den tragenden Säulen und dem Boden verbinden und damit eine statisch wirkungsvolle Raumkomposition erzeugen.

#### Texturierung

Die Texturierung des Bossraumes wurde mit strategischer Farbgebung und Materialwahl umgesetzt, um sowohl die atmosphärische Raumwirkung als auch die psychologische Lenkung des Spielers zu unterstützen. Für die Wandoberflächen wurde ein neutrales Grau gewählt, das Steinoberflächen realistisch darstellt. Durch die Verwendung von verschiedenen Grautönen und Schattierungen wurde eine räumliche Tiefenwirkung erzeugt und bestimmte Bereiche visuell hervorgehoben, um die Raumarchitektur verständlich zu machen.

Die Eingangstür wurde in Brauntönen texturiert, um eine realistische Holzoptik zu simulieren und damit eine authentische Raumwahrnehmung zu fördern. Der Fußbodenteppich wurde bewusst in intensivem Rot texturiert, da diese Farbwahl eine mehrfache psychologische Funktion erfüllt: Zum einen lenkt die warme, auffällige Rotfärbung die Blickrichtung und Bewegungsrichtung des Spielers unmittelbar zur Boss-Position hin. Zum anderen vermittelt die rote Färbung durch ihre kulturelle Assoziation mit Gefahr, Macht und Autorität ein Gefühl von Respekt gegenüber dem Boss-Charakter und unterstreicht damit die narrative Hierarchie des Raums.


#### Optimierung

Die Optimierung des Bossraum-Modells war ein kritischer Aspekt der Entwicklung, um eine stabile Performance und hohe Framerate auf verschiedenen Hardware-Konfigurationen zu gewährleisten. Das gesamte Modellierungsverfahren wurde unter dem Leitprinzip der Low-Poly-Modellierung durchgeführt, um die Polygonanazahl so gering wie möglich zu halten.

**Strategien zur Polygonenreduktion:**
Die Grundstrukturen des Raumes (Boden, Wände, Decke) wurden mit minimaler Geometrie konstruiert. Statt komplexer, organischer Formen wurden hauptsächlich einfache geometrische Primitive und planare Flächen verwendet. Dies reduzierte die Verarbeitungslast erheblich, ohne die visuelle Qualität wesentlich zu beeinträchtigen, da der Low-Poly-Stil ein einheitliches Design-Statement des Spiels darstellt.

**Behandlung von Spalten und Lücken:**
Bei der Minimierung der Polygonanzahl entstanden unvermeidlich kleine Spalten und Lücken in der Wandgeometrie sowie an den Verbindungsstellen zwischen verschiedenen Modellobjekten. Diese Spalten wurden systematisch durch das strategische Platzieren zusätzlicher statischer Dekorationsobjekte wie Wandverzierungen, kleine Säulenabschnitte und architektonische Details aufgefüllt. Dies diente nicht nur als technische Lösung, sondern trug auch zur visuellen Authentizität des Raums bei.

**Wiederverwendung:**
Sich wiederholende Elemente wie Säulen und Wandsegmente wurden als wiederverwendbare Modelle erstellt und mehrfach platziert, statt individuelle Geometrie für jedes Element zu modellieren. Dies reduzierte sowohl die Modellierungszeit als auch die Speicheranforderungen und GPU-Last.

Das resultierende Modell erreichte eine Polygonanazahl von etwa 80.000 Dreiecken für den gesamten Bossraum, was eine optimale Balance zwischen visueller Qualität und Performance-Anforderungen darstellt.

#### Export & Integration in Unreal Engine

Der Export des Bossraum-Modells von Blender nach Unreal Engine 5 erforderte eine sorgfältige Vorbereitung und mehrere aufeinanderfolgende Schritte, um sicherzustellen, dass die Integrität des Modells, die Texturen und die Kollisionsdaten erhalten bleiben.

**Vorbereitung in Blender - Szenen-Organisation:**
Zunächst wurde sichergestellt, dass alle Komponenten des Bossraums korrekt in Blender organisiert waren. Das Modell bestand aus mehreren separaten Objekten (Wände, Säulen, Thronsessel, Tür, Treppen, dekorative Elemente), die zunächst alle aus einzelnen Objekten bestanden. Diese verteilte Struktur ermöglichte Flexibilität bei der Modellierung, musste aber für den Export konsolidiert werden.

**Zusammenfügen mittels Join-Operation:**
Um die Performance während des Exports zu optimieren und die Hierarchie zu vereinfachen, wurden alle Objekte des Bossraums mithilfe der Join-Funktion kombiniert. Dies wurde durchgeführt, indem im Object Mode alle zu vereinigenden Objekte ausgewählt wurden (mittels Shift+Click), das zu behaltende Basisobjekt als letztes ausgewählt wurde, und anschließend die Tastenkombination Ctrl+J zum Zusammenfügen verwendet wurde. Diese Operation reduzierte die Objektanzahl erheblich und vereinfachte die Export-Hierarchie.

**Anwendung von Modifiern:**
Vor dem Export wurden alle angewendeten Modifier (insbesondere Mirror und Solidify) "angewendet" oder "baked", um sicherzustellen, dass diese Transformationen in der FBX-Datei persistent gespeichert werden. Dies geschah durch Auswahl des Modifiers und Klick auf "Apply" im Modifier-Panel.

**FBX-Export-Prozess:**
Der Export wurde mithilfe des Menüpfads `File > Export > FBX (.fbx)` durchgeführt. Dabei öffnete sich der Export-Dialog mit einer umfangreichen Liste von Konfigurationsoptionen. Die folgenden Einstellungen wurden konfiguriert:

- **Scale**: 1.0 (um die Maßstäbe korrekt zu erhalten)
- **Forward Axis**: -Y Forward (Standard für Unreal Engine)
- **Up Axis**: Z Up (Standard für Unreal Engine)
- **Apply Scaling**: FBX All (um Skalierungsinformationen zu bewahren)
- **Smoothing**: Aktiviert (um glatte Übergänge zwischen Flächen zu gewährleisten)
- **Apply Modifiers**: Aktiviert (um alle Modifier in der Geometrie zu berücksichtigen)
- **Bake Animation**: Deaktiviert (da das Modell nicht animiert ist)
- **NLA Strips**: Deaktiviert

**UV-Map und Textur-Erhaltung:**
Es wurde sichergestellt, dass die UV-Maps korrekt in die FBX-Datei exportiert wurden, damit die Texturen in Unreal Engine korrekt auf das Modell angewendet werden konnten. Die Textur-Verweise wurden zwar nicht direkt in der FBX-Datei enthalten, aber die UV-Koordinaten bildeten die Grundlage für die spätere Material-Anwendung in Unreal.

**Import in Unreal Engine 5:**
Nach dem erfolgreichen Export wurde die FBX-Datei in das Unreal Engine 5 Project-Verzeichnis (`Content/Models/`) kopiert. Unreal Engine erkannte die Datei automatisch und importierte sie. Bei der Bestätigung des Imports wurden folgende Parameter konfiguriert:

- **Skeletal Mesh**: Deaktiviert (nicht erforderlich für statische Modelle)
- **Create Physics Asset**: Deaktiviert
- **Create Default Material**: Aktiviert (um automatisch Material-Platzhalter zu erstellen)
- **LOD Settings**: Automatisch (um Level-of-Detail zu generieren)
- **Material Import Method**: Create New Materials
- **Import Textures**: Aktiviert (falls Textur-Dateien vorhanden waren)

**Material-Konfiguration:**
Nach dem Import wurden die automatisch erstellten Materialien überprüft und konfiguriert. Für jede Texturierungszone des Bossraums (Wandstein, Holztür, roter Teppich, etc.) wurden individuelle Materialien erstellt, die die entsprechenden Texturdateien referenzierten. Metallic- und Roughness-Werte wurden für jedes Material gesetzt, um eine realistische Oberflächenwahrnehmung zu ermöglichen.

**Kollisions-Geometrie:**
Die Kollisionsdaten wurden basierend auf der importierten Geometrie automatisch generiert. Zusätzlich wurden Custom Collision Shapes erstellt, um sicherzustellen, dass der Spieler an realistischen Positionen mit dem Umfeld interagiert und nicht durch Wände, Säulen oder den Thron gehen kann.

**Validierung und Tests:**
Nach dem Import wurde das Modell im Level platziert und in verschiedenen Ansichten überprüft (Lit, Unlit, Wireframe). Performance-Tests wurden durchgeführt, um sicherzustellen, dass die Framerate stabil bleibt. Die Lichtsimulation wurde neu berechnet (Baked Lighting), um Beleuchtungseffekte zu optimieren.


\newpage


### Items

//todo

#### Item-Konzept

//todo

#### Funktionen im Spiel

//todo

#### Modellierung

//todo

#### Texturierung

//todo

#### Export & Verwendumg im Spiel

//todo



\newpage

### GUI

Die GUI (Graphical User Interface) bildet die visuelle Schnittstelle zwischen Spieler und Spiel. Sie umfasst alle Bildschirmelemente, die außerhalb der eigentlichen Spielwelt dargestellt werden. Während die GUI alle visuellen Elemente der Benutzeroberfläche bezeichnet, beschreibt das HUD speziell jene Informationsfläche, die während des Spielgeschehens relevante Daten wie Spieler-Lebenspunkte, Ausdauer und Boss-Lebenspunkte anzeigt.

#### Zielsetzung der Benutzeroberfläche

Die primäre Zielsetzung der GUI besteht darin, dem Spieler ausschließlich essentielle Informationen bereitzustellen, ohne ihn dabei durch visuelle Überfrachtung abzulenken. Jedes UI-Element wurde so gestaltet, dass seine Funktion ohne zusätzliche Erklärung verständlich ist. Dies trägt dazu bei, dass sich der Spieler auf das Kampfgeschehen konzentrieren kann, während ihm gleichzeitig alle notwendigen Informationen zur Verfügung stehen.

#### Rolle der GUI im Spielablauf

Die GUI übernimmt verschiedene Funktionen in unterschiedlichen Spielphasen. Zu Beginn leitet das Hauptmenü den Spieler durch die ersten Schritte und ermöglicht den Einstieg ins Spiel. Sobald der Kampf beginnt, übernimmt das HUD die zentrale Rolle: Es zeigt dem Spieler kontinuierlich seine aktuelle Lebenspunkteanzahl sowie seine verfügbare Ausdauer an. Zusätzlich wird die Lebensleiste des Bosses prominent dargestellt, sodass der Spieler den Kampfverlauf nachvollziehen und seine Strategien dynamisch anpassen kann. Nach einem Spieler-Tod erscheint der Death-Screen, der dem Spieler Optionen zur Fortsetzung bietet. Das Statistikmenü ermöglicht es, wichtige Spielinformationen und Errungenschaften einzusehen.

#### Abgrenzung zwischen Spielwelt und Benutzeroberfläche

Die GUI existiert außerhalb der eigentlichen Spielwelt und wird als zweidimensionale Überlagerung im Vordergrund des Bildschirms dargestellt. Diese Trennung zwischen Spielwelt und Benutzeroberfläche wird technisch durch das UMG-Framework realisiert, welches die GUI-Elemente unabhängig von der 3D-Szene rendert. Dadurch bleibt die GUI stets sichtbar und lesbar, unabhängig von Kamerabewegungen oder Spielgeschehen. Diese klare Abgrenzung ermöglicht es dem Spieler, zwischen spielrelevanten Informationen (GUI) und der eigentlichen Spielwelt zu unterscheiden. In der folgenden Abbildung sieht man das HUD im Editor.


![Spieler-HUD mit Lebenspunkten und Ausdauer](img/peissl/praxis/ui-player.png){width=90%}



#### Umsetzung in UMG

Unreal Motion Graphics (UMG) ist das integrierte UI-Framework der Unreal Engine und bildet die technische Grundlage für die Erstellung sämtlicher GUI-Elemente in ConquerTheCastle. UMG bietet einen visuellen Editor, der es ermöglicht, Benutzeroberflächen durch Drag-and-Drop von UI-Komponenten zu erstellen, ohne aufwendige manuelle Code-Implementierung.


**UI-Komponenten und Layout:**
Die einzelnen Widgets bestehen aus verschiedenen Standard-UI-Komponenten:

- **Canvas Panel**: Dient als übergeordneter Container, der absolute und relative Positionierung ermöglicht.
- **Buttons**: Interaktive Schaltflächen mit Hover- und Click-Events, die über Blueprints mit Spiellogik verknüpft sind.
- **Progress Bars**: Visuelle Balken zur Darstellung von Lebenspunkten und Ausdauer, deren Füllstand dynamisch aktualisiert wird.
- **Text Blocks**: Textfelder für Beschriftungen und Informationsdarstellung.
- **Images**: Grafische Elemente zur visuellen Gestaltung und Dekoration.


**Widget-Erstellung:**
Für jedes GUI-Element wurde ein separates Widget erstellt. Ein Widget ist ein wiederverwendbares UI-Element, das sowohl visuelle Komponenten als auch zugehörige Logik enthält. Folgende Widgets wurden implementiert:

- **Mainmenu-Widget**: Enthält Buttons für "Play", "Statistics" und "Quit". Das Layout wurde links ausgerichtet und mit konsistenten Abständen zwischen den Buttons versehen, um dem Spieler sicht auf die Burg zu gewähren.

![Hauptmenü](img/peissl/praxis/mainmenu-ui.png){width=90%}


- **Statistics-Menu-Widget**: Zeigt Spielstatistiken wie gespielete Spiele, Bestzeit und weitere Errungenschaften an.

![Statistikmenü](img/peissl/praxis/statisticsmenu-ui.png){width=90%}


- **HUD-Widget**: Beinhaltet Progress-Bars für Spieler-Lebenspunkte (rot) und Ausdauer (hellblau) sowie die Boss-Lebensleiste.

![Spielerperspektive im Bossraum mit aktiver GUI](img/peissl/praxis/bossroom-player-perspective.png){width=90%}


- **Death-Screen-Widget**: Wird bei Spieler-Tod eingeblendet und bietet Optionen zum Neustart oder zur Rückkehr ins Hauptmenü.

![Death-Screen nach Spieler-Tod](img/peissl/praxis/deathscreen-ui.png){width=90%}



\newpage

### Cutscenes erstellen

Cutscenes dienen in ConquerTheCastle dazu, den Spieler in die Spielwelt einzuführen und wichtige narrative Momente zu inszenieren. Sie schaffen eine atmosphärische Verbindung zwischen den verschiedenen Spielabschnitten und vermitteln dem Spieler das Gefühl einer zusammenhängenden Geschichte. Die Cutscenes wurden mit dem Level Sequencer der Unreal Engine erstellt und über ein Blueprint-System in das Spielgeschehen integriert.

#### Ziel & Einsatz der Cutscenes

Die Cutscenes in ConquerTheCastle verfolgen mehrere spezifische Zielsetzungen:

**Intro-Cutscene:**
Die Intro-Cutscene führt den Spieler in die Spielwelt ein und zeigt einen Überblick über die Umgebung, bevor das eigentliche Gameplay beginnt. Sie erzeugt eine atmosphärische Stimmung und gibt dem Spieler Zeit, sich auf den bevorstehenden Kampf vorzubereiten. Die Cutscene endet mit dem Anzeigen des Hauptmenüs, das dem Spieler Kontrolle über die weitere Spielprogression gibt.

**Bossraum-Cutscene:**
Die zweite Cutscene wird beim Betreten des Bossraums abgespielt und dient als cinematischer Übergang. Sie zeigt den Bossraum aus verschiedenen Perspektiven und lenkt die Aufmerksamkeit des Spielers auf wichtige Elemente wie den Thron und die räumliche Ausdehnung des Kampfareals. Diese Cutscene vermittelt dem Spieler visuell die Größe und Bedeutung des bevorstehenden Bosskampfes.

Durch den Einsatz von Cutscenes wird das Spielerlebnis aufgewertet und erhält eine professionellere, cinematische Qualität. Die Cutscenes fungieren als narrative Klammer, die die einzelnen Spielabschnitte verbindet.

#### Erstellung mit Level Sequencer

Der Level Sequencer ist das zentrale Werkzeug in Unreal Engine für die Erstellung von Cutscenes und cinematischen Sequenzen. Er bietet eine Timeline-basierte Oberfläche, die es ermöglicht, Kamerabewegungen, Aktoren-Transformationen und andere Events zeitlich präzise zu choreographieren.

**Sequencer-Setup:**
Für jede Cutscene wurde eine neue Level Sequence erstellt. Dies geschah über das Menü "Cinematics > Add Level Sequence". Die Sequenzen wurden im Content-Verzeichnis unter einem eigenen Cutscenes-Ordner organisiert, um eine klare Projektstruktur zu gewährleisten.

**Kamera-Integration:**
Zu jeder Sequenz wurde eine Cine Camera Actor hinzugefügt, die als virtuelle Filmkamera fungiert. Die Cine Camera bietet erweiterte Einstellungsmöglichkeiten wie Focal Length (Brennweite), Aperture (Blende) und Focus Settings, die eine filmische Bildgestaltung ermöglichen. Die Kamera wurde im Sequencer als Track hinzugefügt, sodass ihre Position, Rotation und Eigenschaften über die Timeline animiert werden konnten.

**Keyframe-Animation:**
Die Kamerabewegungen wurden durch das Setzen von Keyframes zu bestimmten Zeitpunkten definiert. An kritischen Positionen in der Timeline wurde die Kamera manuell im Viewport positioniert und ein Keyframe gesetzt ("K" gedrückt). Der Sequencer interpoliert automatisch zwischen diesen Keyframes und erzeugt flüssige Kamerabewegungen. Für die Intro-Cutscene wurden mehrere Keyframes gesetzt, um eine schwenkende und fahrtende Bewegung über die Intro-Welt zu erzeugen.

![Intro-Welt mit Kameraposition](img/peissl/praxis/intro-world.png){width=90%}

**Timing und Dauer:**
Die Länge der Cutscenes wurde so gewählt, dass sie informativ sind, ohne den Spielfluss zu unterbrechen. Die Intro-Cutscene wurde auf eine Dauer von etwa 8-10 Sekunden festgelegt, während die Bossraum-Einführungs-Cutscene kürzer gehalten wurde (5-7 Sekunden), da der Spieler bereits im Spielgeschehen ist und schneller ins Gameplay zurückkehren möchte.

#### Kameraführung & Timing

Die Kameraführung in den Cutscenes wurde sorgfältig geplant, um dem Spieler relevante Informationen zu vermitteln und gleichzeitig eine ästhetisch ansprechende Präsentation zu gewährleisten.

**Intro-Cutscene Kameraführung:**
Die Intro-Cutscene beginnt mit einer erhöhten Kameraperspektive, die einen Überblick über die Intro-Welt bietet. Die Kamera bewegt sich langsam und gleichmäßig, um dem Spieler Zeit zu geben, die Umgebung zu erfassen. Die Bewegung folgt einer sanften Kurve, die durch die Interpolation zwischen Keyframes erzeugt wird. Die Kamera senkt sich allmählich ab und richtet sich auf eine zentrale Struktur aus, was einen natürlichen Übergang zum spielbaren Gameplay schafft.

**Bossraum-Cutscene Kameraführung:**
Beim Betreten des Bossraums wird eine Fade-In-Sequenz ausgelöst. Die Kamera startet aus einer Position nahe dem Eingang und schwenkt langsam in Richtung des Throns. Diese Bewegung führt den Blick des Spielers entlang des roten Teppichs und hebt die zentrale Achse des Raums hervor. Die Kamera verweilt kurz auf dem Thron, um die Bedeutung dieser Position zu unterstreichen, bevor sie sanft zur Spielerperspektive übergeht.

![Bossraum Fade-In Cutscene](img/peissl/praxis/bossroom-fadein-cutscene.png){width=90%}

**Timing-Überlegungen:**
Das Timing der Kamerabewegungen wurde so abgestimmt, dass sie weder zu schnell noch zu langsam wirken. Zu schnelle Bewegungen können desorientierend wirken, während zu langsame Bewegungen den Spieler ungeduldig machen. Durch mehrfaches Testen und Anpassen der Keyframe-Positionen und -Zeitpunkte wurde ein ausgewogenes Tempo gefunden.

**Easing und Interpolation:**
Für natürlichere Bewegungen wurden Easing-Funktionen auf die Keyframes angewendet. Statt linearer Interpolation wurde "Ease In" und "Ease Out" verwendet, wodurch die Kamera sanft beschleunigt und abbremst. Dies erzeugt einen cinematischeren Eindruck und vermeidet abrupte Bewegungsänderungen.

#### Trigger & Ablauf im Spiel

Die Integration der Cutscenes in den Spielablauf erfolgt über ein ausgeklügeltes Blueprint-System, das sicherstellt, dass die Cutscenes zum richtigen Zeitpunkt abgespielt werden und nahtlos in das Gameplay übergehen. Das folgende Diagramm zeigt den kompletten Ablauf der Cutscene- und Menü-Logik:

![Kompletter Spielablauf von Cutscene bis Bosskampf](img/peissl/praxis/vollstaendiger-spielablauf.png){width=100%}

**Spielstart und Intro-Sequenz:**
Beim Start des Spiels wird automatisch die Intro-Cutscene gestartet. Dies geschieht im Level-Blueprint des Intro-Levels durch Aufruf der "Play"-Funktion der Level Sequence. Der Ablauf folgt dabei dieser Logik:

1. **Event BeginPlay:** Das Event wird ausgelöst, wenn das Level vollständig geladen ist
2. **Create/Get Level Sequence:** Die Intro-Cutscene Sequence wird referenziert oder erstellt
3. **Play:** Die Sequenz wird gestartet und die Cutscene läuft ab
4. **Stop Motion Camera:** Ein Node stoppt ggf. die Kamerabewegung nach der Cutscene

![Level-Blueprint für Intro-Welt](img/peissl/praxis/code-intro-world.png){width=90%}
![Blueprint-Code zum Start der Cutscene](img/peissl/praxis/code-start-cutscene.png){width=90%}

**Hauptmenü-Erstellung und Anzeige:**
Nach Ablauf der Intro-Cutscene wird das Hauptmenü-Widget erstellt und eingeblendet. Dies wird durch einen "On Finished"-Event des Sequence Players erreicht, der ausgelöst wird, sobald die Cutscene vollständig abgespielt wurde. Der Blueprint führt folgende Schritte durch:

1. **Create Widget:** Das Mainmenu-Widget wird als Instanz erstellt
2. **Add to Viewport:** Das Widget wird zum visuellen Anzeigebereich hinzugefügt
3. **Set Input Mode:** Der Input-Mode wird auf "UI Only" gesetzt
4. **Show Mouse Cursor:** Der Maus-Cursor wird sichtbar gemacht

![Blueprint-Code zur Erstellung des Hauptmenüs](img/peissl/praxis/code-create-mainmenu.png){width=90%}

**Play-Button-Event und Levelüdbergang:**
Wenn der Spieler den "Play"-Button im Hauptmenü betätigt, wird ein Custom Event ausgelöst, das folgende Aktionen koordiniert:

1. **Remove from Parent:** Das Hauptmenü-Widget wird aus dem Viewport entfernt
2. **Set Input Mode:** Der Input-Mode wird auf "Game Only" zurückgesetzt
3. **Hide Mouse Cursor:** Der Maus-Cursor wird ausgeblendet
4. **Load Level (Optional):** Ein Übergangs-Level oder Cutscene kann optional geladen werden

![Logik des Play-Buttons](img/peissl/praxis/logic-play-button.png){width=90%}

**Fortsetzungs-Cutscene (Optional):**
Nach Klick auf den Play-Button kann optional eine kurze Übergangs-Cutscene abgespielt werden, die vom Intro zum Bossraum überleitet. Diese Cutscene kann zusätzliche narrative Elemente enthalten:

![Blueprint zur Fortsetzung der Cutscene](img/peissl/praxis/continiue-cutscene.png){width=90%}

**Bossraum-Eingangs-Cutscene:**
Beim Laden des Bossraum-Levels wird automatisch die Bossraum-Einführungs-Cutscene gestartet. Dies geschieht im Level-Blueprint des Bossraum-Levels über das Event BeginPlay. Die Cutscene zeigt dem Spieler den Raum aus verschiedenen Perspektiven und endet mit einem sanften Übergang zur Spielerperspektive, woraufhin die volle Spielerkontrolle wiederhergestellt wird.

**Spieler-Kontrolle während Cutscenes:**
Während eine Cutscene abgespielt wird, wird dem Spieler die Kontrolle entzogen. Dies geschieht durch Setzen des Input-Modes auf "UI Only" oder "Cinematic". Die Spielfigur wird temporär deaktiviert oder an Ort und Stelle eingefroren, um sicherzustellen, dass der Spieler die Cutscene nicht durch Bewegung unterbrechen kann. Nach Abschluss der Cutscene wird die volle Spielerkontrolle durch Aufruf von entsprechenden Blueprint-Funktionen wiederhergestellt.

**Überspringbarkeit:**
In der aktuellen Implementation sind die Cutscenes nicht überspringbar, da sie kurz gehalten sind und wichtige narrative Informationen vermitteln. Für längere Cutscenes in zukünftigen Erweiterungen könnte eine Skip-Funktion implementiert werden, die durch Drücken einer bestimmten Taste (z.B. ESC oder Space) aktiviert wird und die Cutscene sofort beendet.

**Event-Verkettung:**
Die verschiedenen Events sind sorgfältig miteinander verknüpft, um einen nahtlosen Übergang zwischen Cutscenes, Menüs und Gameplay zu gewährleisten. Dies verhindert, dass Fehler oder ungewünschte Zustände auftreten, wie zum Beispiel das gleichzeitige Anzeigen von Menü und HUD oder die versehentliche Aktivierung von Spielereingaben während einer Cutscene.



