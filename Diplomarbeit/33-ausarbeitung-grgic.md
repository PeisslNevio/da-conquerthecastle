# Teilaufgabe Schüler Grgic
\textauthor{Grgic}

## Theorie

### Warum Unreal Engine gegenüber anderen Engines im Bereich Grafik & Rendering wählen?

#### Allgemein

***Allgemeine Ausrichtung von Unreal Engine***

Unreal Engine ist von Grund auf auf High-End-Grafik ausgelegt. Der Fokus liegt klar auf realistischer Lichtberechnung und physikalisch korrekter Darstellung, anstatt auf vereinfachtem oder sogenanntem „Fake-Lighting“. Die Standard-Workflows orientieren sich stark an professionellen Film-, VFX- und Architektur-Pipelines. Ziel der Unreal Engine ist es, eine möglichst hohe visuelle Qualität bei gleichzeitig geringem manuellem Optimierungsaufwand zu erreichen.

***Gegensatz zu Unity***

Unity ist stärker auf Performance, mobile Plattformen und eine möglichst breite Hardware-Unterstützung ausgelegt. Hochwertige Grafik ist zwar möglich, erfordert jedoch deutlich mehr Konfigurationsaufwand, Erfahrung und zusätzliche Arbeitsschritte. Für das vorliegende Projekt, das eine kleine, überschaubare Spielwelt besitzt, ist diese Optimierung auf mobile Plattformen nicht relevant.

#### Photorealismus & Realismus

***Unreal Engine***

Physikalisch basiertes Rendering (PBR) ist in Unreal Engine standardmäßig aktiviert. Materialien reagieren dadurch realistisch auf Eigenschaften wie:

* Licht
* Rauheit
- Metallizität

Dies ermöglicht die Darstellung glaubwürdiger Oberflächen ohne tiefgehende Shader-Kenntnisse. Bereits mit den Standardwerkzeugen der Engine lassen sich realistische Ergebnisse erzielen, die „out of the box“ eine hohe Qualität besitzen.

***Vergleich zu Unity***

Unity kann ebenfalls photorealistische Ergebnisse liefern, dies ist jedoch hauptsächlich mit der High Definition Render Pipeline (HDRP) möglich. Diese erfordert:

- einen höheren Konfigurationsaufwand  
- detaillierte Shader-Anpassungen  
- zusätzliche manuelle Feinarbeit  

Im Vergleich dazu liefert Unreal Engine vergleichbare oder bessere Ergebnisse deutlich schneller und konsistenter.

#### Nanite – Virtuelle Geometrie

***Unreal Engine***

Nanite ermöglicht die Verwendung extrem hochauflösender Modelle mit Millionen bis Milliarden von Polygonen. Dabei passt die Engine automatisch die Detailstufe der Geometrie an die aktuelle Ansicht an. Eine manuelle Erstellung von LOD-Stufen ist nicht mehr notwendig. Dies reduziert Entwicklungszeit, Fehleranfälligkeit und Asset-Aufwand erheblich, was insbesondere für kleine Teams von großem Vorteil ist.

Nanite eignet sich besonders für:

- Scan-Daten  
- Architekturvisualisierungen  
- detailreiche Spielwelten  

***Vergleich zu Unity***

Unity verwendet ein klassisches LOD-System, bei dem Detailstufen manuell erstellt werden müssen. Die Performance hängt stark von der Optimierung der Assets ab. Ein vergleichbares System zu Nanite ist in Unity nicht in gleicher Form vorhanden.

#### Lumen – Dynamische Global Illumination

***Unreal Engine***

Unreal Engine berechnet mit Lumen die globale Beleuchtung und Reflexionen vollständig in Echtzeit. Das Licht reagiert dynamisch auf:

- bewegte Objekte  
- Zerstörung  
- Tageszeitwechsel  

Ein klassisches Light-Baking ist nicht erforderlich. Dadurch wirken Szenen lebendiger, natürlicher und konsistenter, während gleichzeitig der Iterationsaufwand im Leveldesign deutlich reduziert wird.

***Vergleich zu Unity***

Unity setzt hauptsächlich auf vorab berechnetes Light-Baking. Bei jeder Änderung am Level muss das Licht erneut berechnet werden. Echtzeit-Global-Illumination ist nur eingeschränkt verfügbar und häufig sehr performanceintensiv.

Lumen spart dadurch:

- Zeit  
- Speicherplatz  
- Iterationsaufwand  

#### Post-Processing & Bildqualität

***Unreal Engine***

Unreal Engine bietet eine integrierte Post-Processing-Pipeline mit hochwertigen Effekten wie:

- Bloom (Überstrahlen heller Lichtquellen)  
- Motion Blur (Bewegungsunschärfe)  
- Depth of Field (Tiefenunschärfe wie bei realen Kameras)  
- Film Grain (Simulation analoger Filmkörnung)  

Post-Processing beschreibt die digitale Nachbearbeitung des gerenderten Bildes zur Verbesserung von Atmosphäre und Bildwirkung. Die Effekte sind über sogenannte Post-Process-Volumes steuerbar und sorgen für einen konsistenten, filmischen Look.

***Vergleich zu Unity***

In Unity werden Post-Processing-Effekte häufig über zusätzliche Pakete realisiert. Die Abstimmung ist komplexer und erfordert mehr manuelle Anpassungen, während in Unreal Engine ein cineastischer Look schneller und mit weniger technischen Hürden erreicht wird.

#### Workflow & Produktivität (grafikbezogen)

***Unreal Engine***

Unreal Engine bietet eine sehr realitätsnahe Editor-Vorschau. Das im Editor sichtbare Ergebnis entspricht in der Regel dem finalen Spielbild („What you see is what you get“). Änderungen an Licht, Materialien oder Geometrie sind sofort sichtbar, was iteratives Arbeiten und visuelles Feintuning stark erleichtert.

***Vergleich zu Unity***

In Unity sind häufiger Test-Builds notwendig. Das endgültige Ergebnis hängt stärker von:

- Zielplattform  
- verwendeter Render-Pipeline  
- Build-Einstellungen  

ab, wodurch der Feedback-Zyklus langsamer ist.

---

### Warum Unreal Engine im Bereich Programmierung & Blueprints wählen?

#### Grundidee der Blueprints

Unreal Engine bietet ein vollständig integriertes visuelles Skripting-System. Die Spiellogik wird über node-basierte Graphen abgebildet. Funktionen, Events und Variablen sind grafisch darstellbar, wodurch auf klassischen Textcode verzichtet werden kann. Der Fokus liegt auf Verständlichkeit, Übersichtlichkeit und logischem Aufbau anstatt auf Syntax.

#### Programmieren ohne klassischen Code

Blueprints sind ein zentraler Bestandteil der Unreal Engine und nahtlos in alle Systeme integriert.

**Vorteile:**

- kein zwingendes Vorwissen in C++ erforderlich  
- Einstieg auch ohne Programmierkenntnisse möglich  
- Fehler leichter nachvollziehbar als bei Textcode  
- Logik visuell gut lesbar  

***Vergleich zu Unity***

Unity verwendet primär C#-Skripte. Visuelles Skripting ist optional und weniger tief in die Engine integriert.

#### Node-System & Logikaufbau

***Unreal Engine***

Nodes repräsentieren:

- Funktionen  
- Events  
- Bedingungen  
- Schleifen  

Dabei wird klar zwischen Ablaufsteuerung (Execution Flow) und Datenfluss (Variablen) unterschieden. Auch komplexe Logiken lassen sich ohne lange Code-Dateien umsetzen. Besonders geeignet ist dieses System für:

- Gameplay-Logik  
- Benutzeroberflächen  
- Interaktionen  
- Trigger-Systeme  

***Vergleich zu Unity***

In Unity ist Logik hauptsächlich textbasiert. Visuelle Logiksysteme sind nur über Zusatztools möglich und bieten weniger visuelle Kontrolle über den Ablauf.

#### Ideal für Anfänger & Designer

Unreal Engine erleichtert Anfängern den Einstieg erheblich. Designer können Gameplay-Elemente selbst umsetzen und Anpassungen ohne Programmierer vornehmen. Dies fördert interdisziplinäres Arbeiten und reduziert Abhängigkeiten innerhalb kleiner Teams. Besonders für Diplomarbeiten und Prototypen ist dies ein großer Vorteil.

#### Schnelles Prototyping

***Unreal Engine***

Gameplay-Ideen lassen sich sehr schnell umsetzen. Änderungen sind sofort testbar und erfordern meist kein erneutes Kompilieren. Der iterative Entwicklungsprozess wird dadurch stark beschleunigt.

***Vergleich zu Unity***

In Unity ist nach jeder Codeänderung eine erneute Kompilierung notwendig, wodurch Testzyklen länger dauern.

#### Kombination aus Blueprints & C++

***Unreal Engine***

Unreal Engine erlaubt die Kombination aus C++ und Blueprints. Typischerweise wird die Grundlogik in C++ implementiert, während Feinabstimmungen über Blueprints erfolgen. Performancekritische Bereiche können gezielt ausgelagert werden, was eine hohe Flexibilität für kleine und große Projekte bietet.

***Vergleich zu Unity***

Unity setzt primär auf C# und bietet keine so klare Trennung zwischen Low-Level-Logik und Gameplay-Scripting.

#### Änderungen in Echtzeit sichtbar

***Unreal Engine***

Änderungen an Blueprints sind sofort im Spiel sichtbar. Neustarts oder Builds sind nicht notwendig, was Debugging, Tests und Feinschliff deutlich erleichtert.

***Vergleich zu Unity***

In Unity ist häufiges Stoppen und Neustarten des Play-Modus notwendig, was den Feedback-Zyklus verlangsamt.

### Warum Unreal Engine gegenüber anderen Engines im Bereich Game Development wählen?

#### Allgemeine Einordnung

Unreal Engine ist mittlerweile keine reine Spiele-Engine mehr, sondern eine umfassende Echtzeit-3D-Plattform. Der Fokus liegt auf hochwertiger visueller Darstellung, Simulationen sowie interaktiven Echtzeitsystemen. Einsatzgebiete finden sich vor allem in Industrie, Medien und Forschung. Unity wird zwar ebenfalls in diesen Bereichen eingesetzt, jedoch häufiger für mobile Anwendungen, einfache Spiele oder Trainingsumgebungen. Unreal Engine hingegen ist klar auf High-End-Visualisierung und maximale Bildqualität ausgerichtet.

#### Game Development

***Unreal Engine***

Im Bereich Game Development liegt der Fokus von Unreal Engine insbesondere auf High-End-PC- und Konsolenspielen. Dies zeigt sich durch die realistische Grafikdarstellung, große Spielwelten und moderne Technologien. Features wie Nanite, Lumen und Blueprints eignen sich besonders für atmosphärische Spiele, AAA-nahe Projekte sowie für kleinere Teams mit hohem Qualitätsanspruch.

***Vergleich zu Unity***

Unity ist stärker im mobilen Bereich verbreitet, da geringere Hardwareanforderungen bestehen und eine breitere Plattformunterstützung möglich ist. Für grafisch anspruchsvolle Projekte ist jedoch zusätzlicher Optimierungsaufwand notwendig.

#### Architekturvisualisierung

Unreal Engine wird häufig für Echtzeit-Architekturvisualisierungen und interaktive Gebäudebegehungen eingesetzt. Im Vergleich zu klassischen, statischen Renderbildern bietet Unreal Engine eine deutlich realistischere und interaktive Darstellung.

**Vorteile:**

- realistische Lichtsimulation  
- Interaktion statt statischer Bilder  
- physikalisch korrektes Materialverhalten  
- Echtzeit-Änderungen von:
  - Tageszeit  
  - Beleuchtung  
  - Materialien  

Genutzt wird Unreal Engine unter anderem von:

- Architekturbüros  
- Bauunternehmen  
- Immobilienentwicklern  

#### Film & Animation (Virtual Production)

***Unreal Engine***

Unreal Engine spielt eine zentrale Rolle im Bereich der Virtual Production. Dabei kommen LED-Walls und Echtzeit-Hintergründe zum Einsatz, die klassische Greenscreen-Techniken zunehmend ersetzen.

**Vorteile:**

- Beleuchtung passt sich der virtuellen Umgebung an  
- geringerer Postproduktionsaufwand  
- kosteneffizientere Produktionsprozesse  
- schnellere Entscheidungsfindung  
- Regisseure sehen das finale Bild bereits direkt am Set  

***Vergleich zu klassischen Pipelines***

Traditionell werden Szenen vor Greenscreens aufgenommen und die Hintergründe erst in der Postproduktion hinzugefügt. Unreal Engine ermöglicht diese Schritte bereits während der Aufnahme in Echtzeit.

#### Simulationen

Unreal Engine wird auch für verschiedene Arten von Simulationen eingesetzt. Dazu zählen physikbasierte Simulationen, Trainingsumgebungen sowie Sicherheits- und Gefahrenszenarien. Typische Einsatzbereiche sind Industrie, Forschung, Ausbildung und militärische Simulationen.

**Vorteile:**

- Echtzeit-Feedback  
- realistische Umgebungen  
- kombinierbar mit KI-Systemen  

#### VR / AR

Unreal Engine bietet eine starke Unterstützung für Virtual Reality und Augmented Reality. Die hohe Bildqualität ist besonders wichtig für Immersion und Realismus. Einsatzgebiete sind unter anderem Trainingssimulationen, medizinische Anwendungen und Produktpräsentationen. Aufgrund der hohen grafischen Qualität ergeben sich jedoch auch höhere Hardwareanforderungen. Unity wird daher häufig für einfachere VR-Projekte bevorzugt.

#### Automobilindustrie

Unreal Engine wird auch in der Automobilindustrie eingesetzt, beispielsweise für Fahrzeugvisualisierungen, Design-Reviews und virtuelle Showrooms. In der Praxis ermöglicht Unreal Engine schnellere Entwicklungszyklen, bessere Entscheidungsgrundlagen und eine Reduktion physischer Prototypen.

**Vorteile:**

- realistische Materialien (Lack, Glas, Metall)  
- Echtzeit-Anpassungen von:
  - Farben  
  - Innenausstattung  
  - Beleuchtung  

#### Digitale Zwillinge

Unreal Engine wird zur Erstellung digitaler Zwillinge realer Systeme, Prozesse oder physischer Objekte verwendet. Einsatzgebiete sind unter anderem Smart Cities, Industrieanlagen und Verkehrsmodelle. Diese digitalen Zwillinge kombinieren:

- Echtzeitdaten  
- 3D-Visualisierung  
- Simulation  

Der Mehrwert liegt in der Analyse komplexer Systeme, der Vorhersage von Verhalten sowie der Optimierung realer Prozesse.

---
## Praktische Arbeit
