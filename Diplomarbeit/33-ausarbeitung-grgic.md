# Teilaufgabe Schüler Grgic
\textauthor{Grgic}

## Theorie

### Warum Unreal Engine gegenüber anderen Engines im Bereich Grafik & Rendering wählen?

#### Allgemein

##### Allgemeine Ausrichtung von Unreal Engine

Unreal Engine ist von Grund auf für High-End-Grafik ausgelegt. Der Fokus liegt auf realistischer Lichtberechnung und physikalisch korrekter Darstellung statt auf vereinfachtem Fake Lighting. Die Standard-Workflows orientieren sich stark an professionellen Film-, VFX- und Architektur-Pipelines. Ziel ist eine möglichst hohe visuelle Qualität bei gleichzeitig geringem manuellen Optimierungsaufwand.

##### Gegensatz zu Unity

Unity ist stärker auf Performance, mobile Plattformen und breite Hardware-Unterstützung ausgerichtet. Hochwertige Grafik ist zwar möglich, erfordert jedoch mehr Konfigurationsaufwand, mehr Erfahrung und zusätzliche Arbeitsschritte. Für dieses Projekt mit einer kleinen, überschaubaren Spielwelt ist diese mobile Optimierung nicht entscheidend.

#### Photorealismus & Realismus

##### Unreal Engine

Physikalisch basiertes Rendering (PBR) ist in Unreal Engine standardmäßig aktiv. Materialien reagieren dadurch realistisch auf Licht, Rauheit und Metallizität. Dadurch lassen sich glaubwürdige Oberflächen auch ohne tiefgehende Shader-Kenntnisse umsetzen. Bereits mit den Standardwerkzeugen der Engine sind hochwertige Ergebnisse möglich.

##### Vergleich zu Unity

Unity kann ebenfalls photorealistische Ergebnisse liefern, dies ist jedoch vor allem mit der High Definition Render Pipeline (HDRP) praktikabel. Dafür sind in der Regel ein höherer Konfigurationsaufwand, detaillierte Shader-Anpassungen und zusätzliche manuelle Feinarbeit nötig. Im Vergleich dazu liefert Unreal Engine ähnliche oder bessere Ergebnisse schneller und konsistenter.

#### Nanite - Virtuelle Geometrie

##### Unreal Engine

Nanite ermöglicht die Verwendung extrem hochauflösender Modelle mit Millionen bis Milliarden Polygonen. Die Engine passt die Detailstufe automatisch an die aktuelle Ansicht an. Eine manuelle Erstellung von LOD-Stufen entfällt. Das reduziert Entwicklungszeit, Fehleranfälligkeit und Asset-Aufwand erheblich, was besonders für kleine Teams ein Vorteil ist. Nanite eignet sich insbesondere für Scan-Daten, Architekturvisualisierungen und detailreiche Spielwelten.

##### Vergleich zu Unity

Unity verwendet ein klassisches LOD-System, bei dem Detailstufen manuell erstellt werden müssen. Die Performance hängt dadurch stärker von der Asset-Optimierung ab. Ein direkt vergleichbares System wie Nanite ist in Unity nicht in gleicher Form vorhanden.

#### Lumen - Dynamische Global Illumination

##### Unreal Engine

Mit Lumen berechnet Unreal Engine globale Beleuchtung und Reflexionen vollständig in Echtzeit. Das Licht reagiert dynamisch auf bewegte Objekte, Zerstörung und Tageszeitwechsel. Klassisches Light Baking ist nicht zwingend notwendig. Szenen wirken dadurch lebendiger und konsistenter, während der Iterationsaufwand im Leveldesign sinkt.

##### Vergleich zu Unity

Unity setzt häufig auf vorab berechnetes Light Baking. Bei Änderungen am Level muss das Licht oft neu berechnet werden. Echtzeit-Global-Illumination ist nur eingeschränkt verfügbar und kann performanceintensiv sein. Lumen reduziert dadurch Zeitaufwand, Speicherbedarf und Iterationsaufwand.

#### Post-Processing & Bildqualität

##### Unreal Engine

Unreal Engine bietet eine integrierte Post-Processing-Pipeline mit Effekten wie Bloom, Motion Blur, Depth of Field und Film Grain. Post-Processing beschreibt die digitale Nachbearbeitung des gerenderten Bildes zur Verbesserung von Atmosphäre und Bildwirkung. Die Effekte sind über Post-Process-Volumes steuerbar und ermöglichen einen konsistenten, filmischen Look.

##### Vergleich zu Unity

In Unity werden Post-Processing-Effekte häufig über zusätzliche Pakete integriert. Die Abstimmung ist komplexer und erfordert mehr manuelle Konfiguration. In Unreal Engine lässt sich ein cineastischer Look meist schneller erreichen.

#### Workflow & Produktivität (grafikbezogen)

##### Unreal Engine

Unreal Engine bietet eine realitätsnahe Editor-Vorschau. Das sichtbare Ergebnis entspricht in der Regel dem finalen Spielbild (What you see is what you get). Änderungen an Licht, Materialien oder Geometrie sind sofort sichtbar, was iteratives Arbeiten deutlich beschleunigt.

##### Vergleich zu Unity

In Unity sind häufiger Test-Builds notwendig. Das Endergebnis hängt stärker von Zielplattform, Render-Pipeline und Build-Einstellungen ab, wodurch der Feedback-Zyklus langsamer sein kann.

\newpage

### Warum Unreal Engine im Bereich Programmierung & Blueprints wählen?

#### Grundidee der Blueprints

Unreal Engine bietet ein vollständig integriertes visuelles Skripting-System. Die Spiellogik wird über node-basierte Graphen abgebildet. Funktionen, Events und Variablen sind grafisch darstellbar, wodurch auf klassischen Textcode teilweise verzichtet werden kann. Der Fokus liegt auf Verständlichkeit, Übersichtlichkeit und logischem Aufbau statt auf Syntax.

#### Programmieren ohne klassischen Code

Blueprints sind ein zentraler Bestandteil der Unreal Engine und nahtlos in alle Systeme integriert. Dadurch ist kein zwingendes Vorwissen in C++ erforderlich, ein Einstieg auch ohne tiefe Programmierkenntnisse möglich und die Logik visuell gut lesbar. Fehler lassen sich in vielen Fällen schneller nachvollziehen als bei reinem Textcode.

##### Vergleich zu Unity

Unity verwendet primär C#-Skripte. Visuelles Skripting ist vorhanden, aber weniger tief in die Engine-Workflows integriert.

#### Node-System & Logikaufbau

##### Unreal Engine

Nodes repräsentieren Funktionen, Events, Bedingungen und Schleifen. Dabei wird klar zwischen Ablaufsteuerung (Execution Flow) und Datenfluss (Variablen) unterschieden. Auch komplexe Logiken lassen sich damit ohne lange Code-Dateien strukturieren. Dieses System eignet sich besonders für Gameplay-Logik, Benutzeroberflächen, Interaktionen und Trigger-Systeme.

##### Vergleich zu Unity

In Unity ist Logik primär textbasiert. Visuelle Systeme sind meist Zusatztools und bieten häufig weniger direkte Übersicht über den Ablauf.

#### Ideal für Anfänger & Designer

Unreal Engine erleichtert den Einstieg für Anfänger erheblich. Designer können Gameplay-Elemente selbst umsetzen und Anpassungen ohne direkten Eingriff von Programmierern vornehmen. Das fördert interdisziplinäres Arbeiten und reduziert Abhängigkeiten im Team.

#### Schnelles Prototyping

##### Unreal Engine

Gameplay-Ideen lassen sich schnell umsetzen. Änderungen sind sofort testbar und erfordern oft kein langes Kompilieren. Der iterative Entwicklungsprozess wird dadurch beschleunigt.

##### Vergleich zu Unity

In Unity ist nach Codeänderungen häufig eine erneute Kompilierung nötig, wodurch Testzyklen länger werden.

#### Kombination aus Blueprints & C++

##### Unreal Engine

Unreal Engine erlaubt die gezielte Kombination aus C++ und Blueprints. Grundlogik kann in C++ implementiert werden, während Feinabstimmungen in Blueprints erfolgen. Performancekritische Bereiche lassen sich damit gezielt optimieren.

##### Vergleich zu Unity

Unity setzt primär auf C# und bietet weniger klare Trennung zwischen Low-Level-Logik und visuellem Gameplay-Scripting.

#### Änderungen in Echtzeit sichtbar

##### Unreal Engine

Änderungen an Blueprints sind unmittelbar im Spiel testbar. Zusätzliche Neustarts oder Builds sind oft nicht nötig, was Debugging und Feinschliff erleichtert.

##### Vergleich zu Unity

In Unity ist häufiges Stoppen und Neustarten des Play-Modus notwendig, was den Feedback-Zyklus verlangsamt.

### Warum Unreal Engine gegenüber anderen Engines im Bereich Game Development wählen?

#### Allgemeine Einordnung

Unreal Engine ist heute nicht nur eine Spiele-Engine, sondern eine umfassende Echtzeit-3D-Plattform. Der Schwerpunkt liegt auf hochwertiger visueller Darstellung, Simulationen und interaktiven Echtzeitsystemen. Unity wird ebenfalls in vielen Bereichen eingesetzt, ist aber stärker im mobilen und leichtgewichtigen Bereich verbreitet. Unreal Engine ist klar auf High-End-Visualisierung und hohe Bildqualität ausgerichtet.

#### Game Development

##### Unreal Engine

Im Game Development liegt der Fokus von Unreal Engine besonders auf High-End-PC- und Konsolenspielen. Das zeigt sich in realistischer Grafik, großen Spielwelten und modernen Technologien. Features wie Nanite, Lumen und Blueprints eignen sich besonders für atmosphärische Spiele und Projekte mit hohem Qualitätsanspruch.

##### Vergleich zu Unity

Unity ist im mobilen Bereich stark verbreitet, da geringere Hardwareanforderungen und breite Plattformunterstützung möglich sind. Für grafisch sehr anspruchsvolle Projekte ist jedoch oft zusätzlicher Optimierungsaufwand nötig.

#### Architekturvisualisierung

Unreal Engine wird häufig für Echtzeit-Architekturvisualisierungen und interaktive Gebäudebegehungen eingesetzt. Im Vergleich zu statischen Renderbildern bietet Unreal Engine eine deutlich realistischere und interaktive Darstellung. Vorteile sind dabei eine realistische Lichtsimulation, Interaktion statt rein statischer Darstellung, physikalisch korrektes Materialverhalten sowie Echtzeit-Änderungen von Tageszeit, Beleuchtung und Materialien. Genutzt wird Unreal Engine unter anderem von Architekturbüros, Bauunternehmen und Immobilienentwicklern.

#### Film & Animation (Virtual Production)

##### Unreal Engine

Unreal Engine spielt eine zentrale Rolle in der Virtual Production. LED-Walls und Echtzeit-Hintergründe ersetzen dabei zunehmend klassische Greenscreen-Techniken. Die Beleuchtung passt sich direkt der virtuellen Umgebung an, der Postproduktionsaufwand sinkt, Produktionsprozesse werden kosteneffizienter und Entscheidungen am Set können schneller getroffen werden, weil Regie und Team das Ergebnis direkt während der Aufnahme sehen.

##### Vergleich zu klassischen Pipelines

Traditionell werden Szenen vor Greenscreen aufgenommen und Hintergründe erst in der Postproduktion ergänzt. Mit Unreal Engine können diese Schritte bereits in Echtzeit während der Aufnahme stattfinden.

#### Simulationen

Unreal Engine wird für unterschiedliche Simulationsarten eingesetzt, zum Beispiel physikbasierte Trainingsumgebungen sowie Sicherheits- und Gefahrenszenarien. Typische Einsatzbereiche sind Industrie, Forschung, Ausbildung und militärische Anwendungen. Die Vorteile liegen in Echtzeit-Feedback, realistischen Umgebungen und der guten Kombinierbarkeit mit KI-Systemen.

#### VR / AR

Unreal Engine bietet starke Unterstützung für Virtual Reality und Augmented Reality. Die hohe Bildqualität ist wichtig für Immersion und Realismus. Typische Anwendungsbereiche sind Trainingssimulationen, medizinische Anwendungen und Produktpräsentationen. Die hohe grafische Qualität bringt allerdings höhere Hardwareanforderungen mit sich.

#### Automobilindustrie

Unreal Engine wird auch in der Automobilindustrie eingesetzt, etwa für Fahrzeugvisualisierungen, Design-Reviews und virtuelle Showrooms. In der Praxis ermöglicht das schnellere Entwicklungszyklen, bessere Entscheidungsgrundlagen und eine Reduktion physischer Prototypen. Besonders relevant sind dabei realistische Materialdarstellungen wie Lack, Glas und Metall sowie Echtzeit-Anpassungen von Farben, Innenausstattung und Beleuchtung.

#### Digitale Zwillinge

Unreal Engine wird zur Erstellung digitaler Zwillinge realer Systeme, Prozesse oder Objekte verwendet. Einsatzgebiete sind unter anderem Smart Cities, Industrieanlagen und Verkehrsmodelle. Diese digitalen Zwillinge verbinden Echtzeitdaten, 3D-Visualisierung und Simulation. Der Mehrwert liegt in der Analyse komplexer Systeme, der Vorhersage von Verhalten und der Optimierung realer Prozesse.

\newpage

## Praktische Arbeit

### Übersicht

In diesem Kapitel wird die praktische Umsetzung in Unreal Engine beschrieben. Der Schwerpunkt liegt auf der Architektur des Spiels und den wichtigsten Gameplay-Systemen.

Das Spiel besteht aus mehreren zentralen Komponenten: dem Player-System, der Boss-KI, dem Kampfsystem und verschiedenen Projektilmechaniken. Diese Systeme greifen ineinander, um einen interaktiven und spielerisch fordernden Bosskampf zu ermöglichen.

### Warum Blueprints statt reinem Textcode?

Für die praktische Umsetzung wurde im Gameplay-Bereich bewusst mit Blueprints gearbeitet und nicht ausschließlich mit selbst geschriebenem Textcode (z. B. C++). Der Blueprint-Ansatz ermöglicht eine deutlich schnellere Umsetzung und Iteration bei Gameplay-Features, weil Logik und Datenfluss visuell nachvollziehbar sind und Fehler im Graph oft schnell erkannt werden. Gerade für Prototyping und häufige Änderungen ist dieser Ansatz sehr effizient.

Gleichzeitig hat der Ansatz Grenzen: Große Graphen können bei komplexer Logik unübersichtlich werden, bei stark performancekritischen Systemen ist C++ häufig effizienter und die Wartbarkeit hängt stark von einer sauberen Strukturierung ab.

Selbst geschriebener Textcode bietet dafür mehr Kontrolle bei komplexen und performancekritischen Systemen, skaliert gut in großen Projektstrukturen und lässt sich über klassische Code-Workflows sauber versionieren und reviewen. Der Nachteil ist, dass Prototyping meist langsamer wird, die Einstiegshürde durch Syntax und Debugging höher ist und der Ansatz für Nicht-Programmierer weniger zugänglich ist.

Für dieses Projekt war der Blueprint-Ansatz insgesamt sinnvoll, weil Gameplay-Mechaniken wie Dodge, Angriff, Parry und Hit-Detection schnell testbar und leicht nachvollziehbar umgesetzt werden konnten.

### Erklärung zentraler Unreal-Engine-Begriffe

Ein Blueprint ist ein visuelles Skript in Unreal Engine, mit dem Gameplay-Logik über verbundene Nodes statt über reinen Textcode erstellt wird. Eine Node ist dabei ein einzelner Baustein der Logik, zum Beispiel eine Funktion, eine Bedingung oder ein Event.

Ein Event Graph ist der zentrale Ablaufbereich eines Blueprints, in dem die Laufzeitlogik miteinander verbunden wird. Eine InputAction ist ein in den Projekteinstellungen definierter Eingabebefehl, der auf Tastatur oder Maus gelegt wird und anschließend ein Event auslösen kann.

Ein Branch ist eine if-Abfrage mit den Ausgängen True und False. 

Über einen Cast To wird geprüft, ob ein Objekt zu einer bestimmten Klasse gehört; nur bei erfolgreichem Cast kann auf klassenspezifische Variablen und Funktionen zugegriffen werden.

Ein Actor ist jedes Objekt, das in der Spielwelt existieren kann, zum Beispiel Spieler, Boss oder Projektil. 

Ein Tag ist eine kurze Kennzeichnung wie Enemy oder Reflectable, mit der Objekte in der Logik schnell kategorisiert werden.

Hit-Detection bezeichnet die technische Treffererkennung. Eine Hitbox ist das Kollisionsvolumen für Treffer, hier als Sphere Collision. 
Mit Break Hit Result wird ein Treffer-Objekt aufgeschlüsselt, damit unter anderem der getroffene Actor ausgelesen werden kann.

Launch Character ist eine Funktion, die den Spielercharakter mit einem Impuls bewegt und deshalb für das Dodge-System geeignet ist. Der Animation Mode steuert, wie Animationen abgespielt werden; nach einem Angriff muss dieser wieder korrekt gesetzt werden, damit die Figur nicht in einer Animation hängen bleibt.

Stamina ist die Ausdauer-Ressource für Aktionen wie Dodge oder Angriff. 

Ein Cooldown ist eine kurze Sperrzeit nach einer Aktion, damit Eingaben nicht beliebig oft hintereinander ausgeführt werden können.

### Architektur des Spiels

Die zentralen Klassen der Spielarchitektur sind BP_FirstPersonCharacter, BP_Boss, BP_Projectile und BP_HomingProjectile. BP_FirstPersonCharacter steuert Bewegung, Kamera, Angriff, Stamina und Parry-Logik. BP_Boss verwaltet Boss-Leben, Angriffsabläufe und das Spawnen von Projektilen. Die Projektil-Blueprints übernehmen Flugverhalten, Kollision und Spezialverhalten wie Homing und Reflexion.

### Player-System

#### Bewegung und Grundkonfiguration

Der Spieler wird über BP_FirstPersonCharacter gesteuert. Die Kamera ist an die Blickrichtung gekoppelt, sodass sich die Figur beim horizontalen Drehen mitorientiert. Das eigene Character-Mesh ist für die First-Person-Kamera unsichtbar geschaltet, damit keine störenden Körperteile im Sichtfeld auftauchen. Zusätzlich wurden Bewegungswerte wie Laufgeschwindigkeit und Grundbeschleunigung auf das Kampfsystem abgestimmt.

#### Dodge-System

Das Ausweichsystem (Dodge) basiert auf der Unreal-Engine-Funktion Launch Character und ist direkt mit dem Stamina-System verbunden. Pro Dodge werden 20 Stamina von insgesamt 100 verbraucht. Die Boolean-Variable isDodging verhindert Spam und setzt einen Cooldown von einer Sekunde, wodurch während der Dodge-Aktion kein erneuter Dodge möglich ist. Damit ist das Ausweichen ein bewusst eingesetztes Verteidigungswerkzeug und keine dauerhaft verfügbare Bewegungstechnik.

#### Angriffssystem

Der Angriff wird über ein Action Mapping in den Projekteinstellungen ausgelöst (InputAction Attack auf linker Maustaste). Beim Drücken läuft folgender Ablauf ab:

1. isAttacking wird auf true gesetzt, damit keine überlappenden Angriffe starten.
2. Das Array hitActorsThisSwing wird geleert, damit pro Schlag jeder Actor nur einmal Schaden erhält.
3. Die Schlaganimation wird abgespielt.
4. Pro Schlag werden 10 Stamina abgezogen.
5. Nach 1,0 s wird isAttacking wieder auf false gesetzt.
6. Der Animation Mode wird zurückgesetzt, damit die Figur nicht in der Attack-Animation hängen bleibt.
7. Die Stamina-Regeneration startet erst nach weiteren 1,5 s.

Diese Reihenfolge stellt sicher, dass das Kampfsystem kontrolliert, fair und gut ausbalancierbar bleibt.

#### Hit-Detection (Schlag-Erkennung)

Die Treffererkennung erfolgt über die Funktion Hitdetect. Dafür wird in der Animation ein Knochen ausgewählt, um den während aktiver Angriffsframes eine Hitbox erzeugt wird. Als Beispiel sind Frames zwischen 20 und 35 aktiv. Die Hitbox ist eine unsichtbare Sphere Collision mit einem anpassbaren Standardradius von 20 cm. Da Unreal Engine in Zentimetern rechnet, gilt Radius 1 gleich 1 cm.

Ablauf der Trefferprüfung:

1. Ein Branch (if-Abfrage) prüft, ob die Sphere einen Treffer meldet.
2. Über Break Hit Result wird der getroffene Actor ausgelesen.
3. Es wird geprüft, ob der Actor bereits in hitActorsThisSwing enthalten ist.
4. Falls nicht enthalten, wird er hinzugefügt und weiter verarbeitet.
5. Danach folgt die Tag-Prüfung auf Enemy.
6. Bei Enemy wird geprüft, ob das Interface BPI_Attack implementiert ist.
7. Wenn ja, wird HitReaction ausgelöst.

Damit wird verhindert, dass ein Gegner innerhalb eines einzelnen Schlages mehrfach Schaden erhält.

#### Parry und Projektil-Reflexion

Zusätzlich gibt es beim Angreifen ein kurzes Parry-Fenster. Beim Drücken von InputAction Attack wird parryActive für 0,5 Sekunden auf true gesetzt. Trifft der Spieler in dieser Zeit keinen Enemy, wird geprüft, ob ein reflektierbares Projektil getroffen wurde. Der getroffene Actor muss dafür den Tag Reflectable besitzen, danach wird Cast To BP_HomingProjectile ausgeführt und bei erfolgreichem Cast das Reflect-Event aufgerufen. Der Cast ist notwendig, damit nur Projektile mit passender Klasse reflektiert werden und die projektilspezifische Logik sicher verfügbar ist.

#### Zwischenfazit zum Player-System

Das Player-System kombiniert Bewegung, Ressourcenkontrolle (Stamina), Nahkampf und defensive Mechaniken (Dodge/Parry) zu einem geschlossenen Regelwerk. Durch Cooldowns, Zustandsvariablen und klare Trefferlogik entsteht ein System, das sowohl spielbar als auch technisch nachvollziehbar bleibt.



