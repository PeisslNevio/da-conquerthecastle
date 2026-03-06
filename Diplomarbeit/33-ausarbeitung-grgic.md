# Teilaufgabe Grgic Elias
\textauthor{Grgic}

## Theorie

### Warum Unreal Engine gegenüber anderen Engines im Bereich Grafik & Rendering wählen?

#### Allgemein

##### Allgemeine Ausrichtung von Unreal Engine

Unreal Engine ist von Grund auf für High-End-Grafik ausgelegt. Der Fokus liegt auf realistischer Lichtberechnung und physikalisch korrekter Darstellung statt auf vereinfachtem Fake Lighting. Die Standard-Workflows orientieren sich stark an professionellen Film-, VFX- und Architektur-Pipelines. Ziel ist eine möglichst hohe visuelle Qualität bei gleichzeitig geringem manuellen Optimierungsaufwand. [@unreal_lighting_environment] [@unreal_types_of_lights] [@unreal_virtual_shadow_maps]

##### Gegensatz zu Unity

Unity ist stärker auf Performance, mobile Plattformen und breite Hardware-Unterstützung ausgerichtet. Hochwertige Grafik ist zwar möglich, erfordert jedoch mehr Konfigurationsaufwand, mehr Erfahrung und zusätzliche Arbeitsschritte. Für dieses Projekt mit einer kleinen, überschaubaren Spielwelt ist diese mobile Optimierung nicht entscheidend. [@unity_manual_engine_overview] [@unity_render_pipelines]

#### Photorealismus & Realismus

##### Unreal Engine

Physikalisch basiertes Rendering (PBR) ist in Unreal Engine standardmäßig aktiv. Materialien reagieren dadurch realistisch auf Licht, Rauheit und Metallizität. Dadurch lassen sich glaubwürdige Oberflächen auch ohne tiefgehende Shader-Kenntnisse umsetzen. Bereits mit den Standardwerkzeugen der Engine sind hochwertige Ergebnisse möglich. [@unreal_physically_based_materials] [@unreal_engine_materials_doc] [@unreal_material_editor_user_guide]

\newpage
##### Vergleich zu Unity

Unity kann ebenfalls photorealistische Ergebnisse liefern, dies ist jedoch vor allem mit der High Definition Render Pipeline (HDRP) praktikabel. Dafür sind in der Regel ein höherer Konfigurationsaufwand, detaillierte Shader-Anpassungen und zusätzliche manuelle Feinarbeit nötig. Im Vergleich dazu liefert Unreal Engine ähnliche oder bessere Ergebnisse schneller und konsistenter. [@unity_render_pipelines] [@unity_high_definition_render_pipeline] [@unity_physically_based_shading_standard_shader] [@unity_materials_manual]

#### Nanite - Virtuelle Geometrie

##### Unreal Engine

Nanite ermöglicht die Verwendung extrem hochauflösender Modelle mit Millionen bis Milliarden Polygonen. Die Engine passt die Detailstufe automatisch an die aktuelle Ansicht an. Eine manuelle Erstellung von LOD-Stufen entfällt. Das reduziert Entwicklungszeit, Fehleranfälligkeit und Asset-Aufwand erheblich, was besonders für kleine Teams ein Vorteil ist. Nanite eignet sich insbesondere für Scan-Daten, Architekturvisualisierungen und detailreiche Spielwelten. [@unreal_nanite_virtualized_geometry]

##### Vergleich zu Unity

Unity verwendet ein klassisches LOD-System, bei dem Detailstufen manuell erstellt werden müssen. Die Performance hängt dadurch stärker von der Asset-Optimierung ab. Ein direkt vergleichbares System wie Nanite ist in Unity nicht in gleicher Form vorhanden. [@unity_render_pipelines] [@unity_deferred_rendering_path]

#### Lumen - Dynamische Global Illumination

##### Unreal Engine

Mit Lumen berechnet Unreal Engine globale Beleuchtung und Reflexionen vollständig in Echtzeit. Das Licht reagiert dynamisch auf bewegte Objekte, Zerstörung und Tageszeitwechsel. Klassisches Light Baking ist nicht zwingend notwendig. Szenen wirken dadurch lebendiger und konsistenter, während der Iterationsaufwand im Leveldesign sinkt. [@unreal_lumen_global_illumination_reflections]

##### Vergleich zu Unity

Unity setzt häufig auf vorab berechnetes Light Baking. Bei Änderungen am Level muss das Licht oft neu berechnet werden. Echtzeit-Global-Illumination ist nur eingeschränkt verfügbar und kann performanceintensiv sein. Lumen reduziert dadurch Zeitaufwand, Speicherbedarf und Iterationsaufwand. [@unity_lighting_overview] [@unity_deferred_rendering_path]

\newpage
#### Post-Processing & Bildqualität

##### Unreal Engine

Unreal Engine bietet eine integrierte Post-Processing-Pipeline mit Effekten wie Bloom, Motion Blur, Depth of Field und Film Grain. Post-Processing beschreibt die digitale Nachbearbeitung des gerenderten Bildes zur Verbesserung von Atmosphäre und Bildwirkung. Die Effekte sind über Post-Process-Volumes steuerbar und ermöglichen einen konsistenten, filmischen Look. [@unreal_post_process_effects] [@unreal_anti_aliasing_upscaling]

##### Vergleich zu Unity

In Unity werden Post-Processing-Effekte häufig über zusätzliche Pakete integriert. Die Abstimmung ist komplexer und erfordert mehr manuelle Konfiguration. In Unreal Engine lässt sich ein cineastischer Look meist schneller erreichen. [@unity_post_processing_overview] [@unity_post_processing_antialiasing]

#### Workflow & Produktivität (grafikbezogen)

##### Unreal Engine

Unreal Engine bietet eine realitätsnahe Editor-Vorschau. Das sichtbare Ergebnis entspricht in der Regel dem finalen Spielbild (What you see is what you get). Änderungen an Licht, Materialien oder Geometrie sind sofort sichtbar, was iteratives Arbeiten deutlich beschleunigt. Für die Bewertung von Laufzeitverhalten und grafischer Skalierung stehen zusätzlich integrierte Profiling- und Scalability-Werkzeuge zur Verfügung. [@unreal_performance_profiling_configuration] [@unreal_scalability_reference]

##### Vergleich zu Unity

In Unity sind häufiger Test-Builds notwendig. Das Endergebnis hängt stärker von Zielplattform, Render-Pipeline und Build-Einstellungen ab, wodurch der Feedback-Zyklus langsamer sein kann. Für die Analyse stehen der Unity Profiler sowie die Quality Settings zur Verfügung. [@unity_profiler_manual] [@unity_quality_settings] [@unity_universal_render_pipeline]

\newpage

### Warum Unreal Engine im Bereich Programmierung & Blueprints wählen?

#### Grundidee der Blueprints

Unreal Engine bietet ein vollständig integriertes visuelles Skripting-System. Die Spiellogik wird über nodebasierte Graphen abgebildet. Funktionen, Events und Variablen sind grafisch darstellbar, wodurch auf klassischen Textcode teilweise verzichtet werden kann. Der Fokus liegt auf Verständlichkeit, Übersichtlichkeit und logischem Aufbau statt auf Syntax.

#### Programmieren ohne klassischen Code

Blueprints sind ein zentraler Bestandteil der Unreal Engine und nahtlos in alle Systeme integriert. Dadurch ist kein zwingendes Vorwissen in C++ erforderlich, ein Einstieg auch ohne tiefe Programmierkenntnisse möglich und die Logik visuell gut lesbar. Fehler lassen sich in vielen Fällen schneller nachvollziehen als bei reinem Textcode.

##### Vergleich zu Unity

Unity verwendet primär C#-Skripte. Visuelles Skripting ist vorhanden, aber weniger tief in die Engine-Workflows integriert. [@unity_manual_engine_overview]

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

Unreal Engine ist heute nicht nur eine Spiele-Engine, sondern eine umfassende Echtzeit-3D-Plattform. Der Schwerpunkt liegt auf hochwertiger visueller Darstellung, Simulationen und interaktiven Echtzeitsystemen. Unity wird ebenfalls in vielen Bereichen eingesetzt, ist aber stärker im mobilen und leichtgewichtigen Bereich verbreitet. Unreal Engine ist klar auf High-End-Visualisierung und hohe Bildqualität ausgerichtet. [@unity_manual_engine_overview] [@unreal_lighting_environment] [@unreal_engine_materials_doc]

#### Game Development

##### Unreal Engine

Im Game Development liegt der Fokus von Unreal Engine besonders auf High-End-PC- und Konsolenspielen. Das zeigt sich in realistischer Grafik, großen Spielwelten und modernen Technologien. Features wie Nanite, Lumen und Blueprints eignen sich besonders für atmosphärische Spiele und Projekte mit hohem Qualitätsanspruch. [@unreal_nanite_virtualized_geometry] [@unreal_lumen_global_illumination_reflections]

##### Vergleich zu Unity

Unity ist im mobilen Bereich stark verbreitet, da geringere Hardwareanforderungen und breite Plattformunterstützung möglich sind. Für grafisch sehr anspruchsvolle Projekte ist jedoch oft zusätzlicher Optimierungsaufwand nötig. [@unity_manual_engine_overview] [@unity_render_pipelines]

#### Architekturvisualisierung

Unreal Engine wird häufig für Echtzeit-Architekturvisualisierungen und interaktive Gebäudebegehungen eingesetzt. Im Vergleich zu statischen Renderbildern bietet Unreal Engine eine deutlich realistischere und interaktive Darstellung. Vorteile sind dabei eine realistische Lichtsimulation, Interaktion statt rein statischer Darstellung, physikalisch korrektes Materialverhalten sowie Echtzeit-Änderungen von Tageszeit, Beleuchtung und Materialien. Genutzt wird Unreal Engine unter anderem von Architekturbüros, Bauunternehmen und Immobilienentwicklern. [@unreal_lighting_environment] [@unreal_engine_materials_doc] [@unreal_post_process_effects]

\newpage
#### Film & Animation (Virtual Production)

##### Unreal Engine

Unreal Engine spielt eine zentrale Rolle in der Virtual Production. LED-Walls und Echtzeit-Hintergründe ersetzen dabei zunehmend klassische Greenscreen-Techniken. Die Beleuchtung passt sich direkt der virtuellen Umgebung an, der Postproduktionsaufwand sinkt, Produktionsprozesse werden kosteneffizienter und Entscheidungen am Set können schneller getroffen werden, weil Regie und Team das Ergebnis direkt während der Aufnahme sehen.

##### Vergleich zu klassischen Pipelines

Traditionell werden Szenen vor Greenscreen aufgenommen und Hintergründe erst in der Postproduktion ergänzt. Mit Unreal Engine können diese Schritte bereits in Echtzeit während der Aufnahme stattfinden.

#### Simulationen

Unreal Engine wird für unterschiedliche Simulationsarten eingesetzt, zum Beispiel physikbasierte Trainingsumgebungen sowie Sicherheits- und Gefahrenszenarien. Typische Einsatzbereiche sind Industrie, Forschung, Ausbildung und militärische Anwendungen. Die Vorteile liegen in Echtzeit-Feedback, realistischen Umgebungen und der guten Kombinierbarkeit mit KI-Systemen.

#### VR / AR

Unreal Engine bietet starke Unterstützung für Virtual Reality und Augmented Reality. Die hohe Bildqualität ist wichtig für Immersion und Realismus. Typische Anwendungsbereiche sind Trainingssimulationen, medizinische Anwendungen und Produktpräsentationen. Die hohe grafische Qualität bringt allerdings höhere Hardwareanforderungen mit sich.

\newpage
#### Automobilindustrie

Unreal Engine wird auch in der Automobilindustrie eingesetzt, etwa für Fahrzeugvisualisierungen, Design-Reviews und virtuelle Showrooms. In der Praxis ermöglicht das schnellere Entwicklungszyklen, bessere Entscheidungsgrundlagen und eine Reduktion physischer Prototypen. Besonders relevant sind dabei realistische Materialdarstellungen wie Lack, Glas und Metall sowie Echtzeit-Anpassungen von Farben, Innenausstattung und Beleuchtung. [@unreal_engine_materials_doc] [@unreal_lighting_environment]

#### Digitale Zwillinge

Unreal Engine wird zur Erstellung digitaler Zwillinge realer Systeme, Prozesse oder Objekte verwendet. Einsatzgebiete sind unter anderem Smart Cities, Industrieanlagen und Verkehrsmodelle. Diese digitalen Zwillinge verbinden Echtzeitdaten, 3D-Visualisierung und Simulation. Der Mehrwert liegt in der Analyse komplexer Systeme, der Vorhersage von Verhalten und der Optimierung realer Prozesse.

\newpage

## Praktische Arbeit

### Übersicht

In diesem Kapitel wird die praktische Umsetzung in Unreal Engine beschrieben. Der Schwerpunkt liegt auf der Architektur des Spiels und den wichtigsten Gameplay-Systemen.

Das Spiel besteht aus mehreren zentralen Komponenten: dem Player-System, der Boss-KI, dem Kampfsystem und verschiedenen Projektilmechaniken. Diese Systeme greifen ineinander, um einen interaktiven und spielerisch fordernden Bosskampf zu ermöglichen.

### Lernquellen, Eigenleistung und Vorgehen

Ein großer Teil der praktischen Arbeitszeit bestand aus dem Durcharbeiten und direkten Mitumsetzen von YouTube-Tutorials zu Animation, Combat, KI, Projektilen, Kamera und allgemeinen Unreal-Workflows. Die Videos wurden nicht nur angesehen, sondern in wesentlichen Teilen aktiv nachgebaut und auf die eigene Projektstruktur übertragen. [@youtube_tnzv7kqpaio] [@youtube_0bo2yoirday] [@youtube_c02yvlqf0gs] [@youtube_jgwini9_xbu] [@youtube_l9qixi858ag] [@youtube_rkhm862pwku] [@youtube_wuxvq6at6pe] [@youtube_1xjglkrb4_m] [@youtube_xm_7m5fw1hu] [@youtube_npnojek7w58] [@youtube_wz11yqdidfa] [@youtube_eh2onheltga] [@youtube_hsbziqfyzw0]

Während der Umsetzung traten viele Fehler auf. Zusätzlich wurde stellenweise experimentell im Stil von Vibe-Coding gearbeitet, um neue Ideen schnell auszuprobieren. Eine zentrale Herausforderung war dabei, neue Funktionen sauber mit bereits bestehenden Systemen zu verbinden, ohne vorhandene Abläufe zu zerstören.

Jede relevante Änderung wurde unmittelbar im Spiel getestet: Der entsprechende Abschnitt wurde gestartet und anschließend geprüft, ob das Verhalten wie erwartet funktioniert. Dieser iterative Testprozess war ein fester Bestandteil der praktischen Entwicklung.

### Warum Blueprints statt reinem Textcode?

Für die praktische Umsetzung wurde im Gameplay-Bereich bewusst mit Blueprints gearbeitet und nicht ausschließlich mit selbst geschriebenem Textcode (z. B. C++). Der Blueprint-Ansatz ermöglicht eine deutlich schnellere Umsetzung und Iteration bei Gameplay-Features, weil Logik und Datenfluss visuell nachvollziehbar sind und Fehler im Graph oft schnell erkannt werden. Gerade für Prototyping und häufige Änderungen ist dieser Ansatz sehr effizient.

Gleichzeitig hat der Ansatz Grenzen: Große Graphen können bei komplexer Logik unübersichtlich werden, bei stark performancekritischen Systemen ist C++ häufig effizienter und die Wartbarkeit hängt stark von einer sauberen Strukturierung ab.

Selbst geschriebener Textcode bietet dafür mehr Kontrolle bei komplexen und performancekritischen Systemen, skaliert gut in großen Projektstrukturen und lässt sich über klassische Code-Workflows sauber versionieren und reviewen. Der Nachteil ist, dass Prototyping meist langsamer wird, die Einstiegshürde durch Syntax und Debugging höher ist und der Ansatz für Nicht-Programmierer weniger zugänglich ist.

Für dieses Projekt war der Blueprint-Ansatz insgesamt sinnvoll, weil Gameplay-Mechaniken wie Dodge, Angriff, Parry und Hit-Detection schnell testbar und leicht nachvollziehbar umgesetzt werden konnten.

### Erklärung zentraler Unreal-Engine-Begriffe

Ein Blueprint ist ein visuelles Skript in Unreal Engine, mit dem Gameplay-Logik über verbundene Nodes statt über reinen Textcode erstellt wird. Eine Node ist dabei ein einzelner Baustein der Logik, zum Beispiel eine Funktion, eine Bedingung oder ein Event.

Ein Event Graph ist der zentrale Ablaufbereich eines Blueprints, in dem die Laufzeitlogik miteinander verbunden wird. Eine InputAction ist ein in den Projekteinstellungen definierter Eingabebefehl, der auf Tastatur oder Maus gelegt wird und anschließend ein Event auslösen kann.

BeginPlay ist ein Start-Event, das beim Laden eines Actors in die Spielwelt automatisch einmal ausgeführt wird.

Ein Branch ist eine If-Abfrage mit den Ausgängen True und False.

Über einen Cast To wird geprüft, ob ein Objekt zu einer bestimmten Klasse gehört; nur bei erfolgreichem Cast kann auf klassenspezifische Variablen und Funktionen zugegriffen werden.

Ein Interface legt fest, welche Funktionen eine Klasse bereitstellen muss. Damit kann zur Laufzeit einheitlich geprüft werden, ob ein Actor eine bestimmte Reaktion unterstützt.

Ein Actor ist jedes Objekt, das in der Spielwelt existieren kann, zum Beispiel Spieler, Boss oder Projektil.

Eine Referenz ist eine gespeicherte Verknüpfung auf ein vorhandenes Objekt, damit dessen Funktionen und Variablen direkt verwendet werden können.

Ein Tag ist eine kurze Kennzeichnung wie Enemy oder Reflectable, mit der Objekte in der Logik schnell kategorisiert werden.

Hit-Detection bezeichnet die technische Treffererkennung. Eine Hitbox ist das Kollisionsvolumen für Treffer, hier als Sphere Collision.
Mit Break Hit Result wird ein Treffer-Objekt aufgeschlüsselt, damit unter anderem der getroffene Actor ausgelesen werden kann.

Ein Overlap-Event wird ausgelöst, wenn sich zwei Kollisionskomponenten berühren. Es eignet sich für Trigger-Logik wie das zeitlich begrenzte Parry-Fenster.

Launch Character ist eine Funktion, die den Spielercharakter mit einem Impuls bewegt und deshalb für das Dodge-System geeignet ist. Der Animation Mode steuert, wie Animationen abgespielt werden; nach einem Angriff muss dieser wieder korrekt gesetzt werden, damit die Figur nicht in einer Animation hängen bleibt.

Ein Widget ist ein Benutzeroberflächen-Element. Add to Viewport bedeutet, dass dieses Element sichtbar auf dem Bildschirm angezeigt wird.

Set Timer by Event ist eine Funktion, mit der ein Event nach einem Intervall einmalig oder wiederholt ausgeführt wird.

Set Timer by Function Name ruft eine Funktion über ihren Namen in einem definierten Intervall auf, bis der Timer explizit gestoppt wird.

AI Move To ist eine Navigationsfunktion für KI-gesteuerte Figuren. Dabei bewegt sich die Figur zu einem Zielpunkt oder Ziel-Actor, bis der Akzeptanzradius erreicht ist.

Ein AI Controller steuert die Bewegungs- und Entscheidungslogik einer KI-Figur.

Ein For Loop ist eine Schleife mit Start- und Endindex. Der enthaltene Ablauf wird für jeden Indexwert einmal ausgeführt.

Length liefert die Anzahl der Einträge in einem Array.

Random Float in Range erzeugt einen Zufallswert in einem festgelegten Zahlenbereich, zum Beispiel zwischen 0 und 1.

Ein Timer Handle ist eine Referenz auf einen laufenden Timer. Damit kann dieser Timer später gezielt beendet oder zurückgesetzt werden.

Do Once ist ein Kontrollknoten, der einen Ablauf nur einmal ausführt, bis er über einen Reset wieder freigegeben wird.

Clear and Invalidate Timer by Handle beendet einen laufenden Timer und macht den zugehörigen Timer Handle ungültig.

Vector Length berechnet aus einem Geschwindigkeitsvektor den Betrag der Geschwindigkeit als einzelnen Zahlenwert.

Normalize normiert einen Vektor auf die Länge 1 und behält dabei nur die Richtung bei.

Ein Target Point ist ein berechneter Zielpunkt im Raum, der für präziseres Ausrichten von Projektilen verwendet wird.

Is Valid prüft, ob eine Objekt-Referenz vorhanden und zur Laufzeit noch gültig ist. Damit werden Zugriffe auf ungültige Ziele verhindert.

Apply Damage übergibt einen Schadenswert an ein Zielobjekt. Der Event Instigator bezeichnet den verantwortlichen Controller, Damage Causer das konkrete verursachende Objekt, zum Beispiel ein Projektil.

Die Projectile Movement Component steuert die Flugbewegung eines Projektils. Velocity ist dabei der Geschwindigkeitsvektor, also Richtung und Stärke der Bewegung.

Ein Homing Projectile ist ein Projektil, das sein Ziel während des Fluges aktiv nachverfolgt.

Die Homing Target Component ist die Zielkomponente, auf die ein Homing-Projektil fortlaufend ausgerichtet wird.

Get All Actors of Class liefert alle Instanzen einer bestimmten Klasse in der aktuellen Spielwelt. Über den Indexzugriff kann daraus gezielt eine Instanz weiterverwendet werden.

Boss Payback ist ein projektspezifisches Event im Boss-Blueprint, das als Reaktion auf ein erfolgreich reflektiertes Projektil ausgeführt wird.

Stamina ist die Ausdauer-Ressource für Aktionen wie Dodge oder Angriff.

Ein Cooldown ist eine kurze Sperrzeit nach einer Aktion, damit Eingaben nicht beliebig oft hintereinander ausgeführt werden können.

DrainStamina und GainStamina sind Events zur zeitbasierten Steuerung der Ausdauer. DrainStamina reduziert den Wert kontinuierlich, GainStamina stellt ihn schrittweise wieder her.

Ragdoll Physics bedeutet, dass auf das Skelett-Mesh eines Charakters Physik angewendet wird. Der Körper fällt dann physikalisch korrekt zu Boden und signalisiert den Todeszustand.

### Architektur des Spiels

Die zentralen Klassen der Spielarchitektur sind BP_FirstPersonCharacter, BP_Boss, BP_Projectile und BP_HomingProjectile. BP_FirstPersonCharacter steuert Bewegung, Kamera, Angriff, Stamina und Parry-Logik. BP_Boss verwaltet Boss-Leben, Angriffsabläufe und das Spawnen von Projektilen. Die Projektil-Blueprints übernehmen Flugverhalten, Kollision und Spezialverhalten wie Homing und Reflexion.

### Gestaltung der Umgebung

Zu Beginn der praktischen Arbeit wurde die Spielumgebung visuell aufgebaut und abgestimmt. Dazu gehörten die grundlegende Lichtstimmung, der Sonnenstand, ein leichter Nebel sowie weitere Atmosphären-Einstellungen, damit die Szene von Anfang an die gewünschte Wirkung erzielt.

\newpage
### Player-System

#### Bewegung und Grundkonfiguration

Der Spieler wird über BP_FirstPersonCharacter gesteuert. Beim Start des Spiels wird der Charakter initialisiert. Dabei wird die vertikale Kamerabewegung auf einen Bereich von minus 45 bis plus 45 Grad begrenzt, damit die Blicksteuerung kontrollierbar bleibt. Zusätzlich wird eine Referenz auf den Boss gesetzt, um während des Kampfs direkt auf relevante Funktionen und Zustände zugreifen zu können. Das Frontend wird initialisiert und eingeblendet. Danach werden Leben und Ausdauer auf ihre Startwerte gesetzt.

Die Kamera ist an die Blickrichtung gekoppelt, sodass sich die Figur beim horizontalen Drehen mitorientiert. Das eigene Character-Mesh ist für die First-Person-Kamera unsichtbar geschaltet, damit keine störenden Körperteile im Sichtfeld auftauchen. Zusätzlich wurden Bewegungswerte wie Laufgeschwindigkeit und Grundbeschleunigung auf das Kampfsystem abgestimmt.

#### Stamina-System

Das Sprinten ist direkt an die Ausdauerverwaltung gekoppelt. Beim Event StartSprinting wird Max Walk Speed auf 600 gesetzt, isSprinting auf true gesetzt und anschließend geprüft, ob sich der Charakter am Boden befindet. Nur wenn diese Bedingung erfüllt ist, startet das Event DrainStamina.

DrainStamina reduziert currentStamina kontinuierlich um 2 Punkte pro Sekunde. Nach jeder Änderung wird die Benutzeroberfläche aktualisiert, damit der aktuelle Wert korrekt angezeigt wird. Sobald currentStamina den Wert 0 erreicht, wird StopSprinting ausgelöst.

StopSprinting setzt Max Walk Speed auf 300 zurück, setzt isSprinting auf false und startet anschließend GainStamina. Dieses Event erhöht currentStamina mit 1 Punkt pro Sekunde. Dabei wird fortlaufend geprüft, ob currentStamina bereits maxStamina erreicht hat. Solange der Maximalwert nicht erreicht ist, wird zusätzlich abgefragt, ob der Spieler aktuell sprintet oder dodged. Nur wenn beide Zustände nicht aktiv sind, wird die Regeneration weitergeführt.

\newpage
#### Dodge-System

Das Ausweichsystem (Dodge) basiert auf der Unreal-Engine-Funktion Launch Character und ist direkt mit dem Stamina-System verbunden. Pro Dodge werden 20 Stamina von insgesamt 100 verbraucht. Die Boolean-Variable isDodging verhindert eine wiederholte Ausführung in sehr kurzer Zeit und setzt einen Cooldown von einer Sekunde, wodurch während der Dodge-Aktion kein erneuter Dodge möglich ist. Damit ist das Ausweichen ein bewusst eingesetztes Verteidigungswerkzeug und keine dauerhaft verfügbare Bewegungstechnik.

#### Angriffssystem

Der Angriff wird über ein Action Mapping in den Projekteinstellungen ausgelöst, konkret über InputAction Attack auf der linken Maustaste. Beim Start des Angriffs wird zunächst isAttacking auf true gesetzt, damit keine überlappenden Angriffe parallel ausgelöst werden können. Danach wird das Array hitActorsThisSwing geleert, sodass innerhalb eines einzelnen Schlages jeder Actor nur einmal verarbeitet wird. Anschließend wird die Schlaganimation abgespielt und pro Angriff werden 10 Stamina abgezogen.

Nach einem zeitlichen Fenster von 1,0 Sekunden wird isAttacking wieder auf false gesetzt. Direkt danach wird der Animation Mode zurückgesetzt, damit die Figur nicht in der Angriffsanimation verbleibt. Die Stamina-Regeneration startet bewusst verzögert und wird erst nach weiteren 1,5 Sekunden wieder freigegeben. Diese Abfolge sorgt dafür, dass das Kampfsystem kontrolliert, fair und technisch stabil bleibt.

\newpage
#### Hit-Detection (Schlag-Erkennung)

Die Treffererkennung erfolgt über die Funktion Hitdetect. Dafür wird in der Animation ein Knochen ausgewählt, um den während aktiver Angriffsframes eine Hitbox erzeugt wird. Als Beispiel sind Frames zwischen 20 und 35 aktiv. Die Hitbox ist eine unsichtbare Sphere Collision mit einem anpassbaren Standardradius von 20 cm. Da Unreal Engine in Zentimetern rechnet, gilt Radius 1 gleich 1 cm.

Die eigentliche Prüfung beginnt mit einem Branch, der feststellt, ob die Sphere einen Treffer meldet. Bei einem Treffer wird über Break Hit Result der getroffene Actor ausgelesen und mit dem Array hitActorsThisSwing abgeglichen. Ist der Actor dort noch nicht enthalten, wird er ergänzt und erst danach weiterverarbeitet. Im nächsten Schritt wird geprüft, ob der Actor den Tag Enemy besitzt. Trifft das zu, folgt zusätzlich die Prüfung, ob das Interface BPI_Attack implementiert ist. Nur wenn diese Bedingung ebenfalls erfüllt ist, wird HitReaction ausgelöst.

Durch diese mehrstufige Filterung wird verhindert, dass ein Gegner innerhalb eines einzelnen Schlages mehrfach Schaden erhält oder dass ungeeignete Trefferobjekte in die Schadenslogik gelangen.

#### Parry und Projektil-Reflexion

Beim Drücken von InputAction Attack wird zusätzlich ein Parry-Fenster gestartet. Dabei wird parryActive auf true gesetzt und die Collision-Komponente ParryCollider aktiviert. Nach einem Delay von 0,5 Sekunden wird parryActive wieder auf false gesetzt und ParryCollider deaktiviert.

Wenn ParryCollider in diesem Zeitfenster mit einem Homing-Projektil überlappt, wird ein Cast To BP_HomingProjectile ausgeführt. Bei erfolgreichem Cast wird das Event Reflect aufgerufen, wodurch das Projektil auf den Boss zurückgelenkt wird.

\newpage
#### HitReaction und Todeszustand

Das Event HitReaction wird im Kampf vom Boss verwendet, wenn der Spieler getroffen wird. Dabei wird der Lebenswert reduziert und anschließend geprüft, ob Leben kleiner oder gleich 0 ist. Ist diese Bedingung erfüllt, werden Ragdoll Physics aktiviert und der Spielercharakter ist tot.

#### Zwischenfazit zum Player-System

Das Player-System kombiniert Bewegung, Ressourcenkontrolle (Stamina), Nahkampf und defensive Mechaniken (Dodge/Parry) zu einem geschlossenen Regelwerk. Durch Cooldowns, Zustandsvariablen und klare Trefferlogik entsteht ein System, das sowohl spielbar als auch technisch nachvollziehbar bleibt.

### Boss-System

#### Initialisierung und BeginPlay

Der Boss wird beim Spielstart im Event BeginPlay initialisiert. Zunächst wird über Get Player Character und Cast To BP_FirstPersonCharacter eine Player-Referenz gesetzt, damit der Boss auf den Spieler zugreifen kann. Danach folgt ein kurzes Delay von 1,0 Sekunden, anschließend wird das Bossbar-Widget erstellt und über Add to Viewport sichtbar eingeblendet.

Im nächsten Schritt wird das Widget über Initialize Boss mit der Boss-Instanz verknüpft. Anschließend werden die Lebenswerte gesetzt, wobei Max Health Boss auf 500 initialisiert wird und Current Health Boss zu Beginn auf den Maximalwert gesetzt ist. Direkt danach wird E Boss Health Updated aufgerufen, damit die Bossbar den korrekten Startwert anzeigt.

Nach dem Erstellen der Bossbar folgt ein weiteres Delay von 5,0 Sekunden. Danach wird ein Timer gestartet, der das Event FollowPlayer periodisch ausführt. Der Timer läuft im Intervall von 0,2 Sekunden und hält damit die Verfolgungslogik des Bosses kontinuierlich aktiv.

\newpage
#### BossHitReaction

Die BossHitReaction wird vom Player über das Angriffssystem ausgelöst, sobald ein Treffer am Boss registriert wurde. Im Event HitReaction werden dem Boss pro Treffer 10 Lebenspunkte abgezogen. Danach wird E Boss Health Updated erneut aufgerufen, damit die Bossbar den reduzierten Lebenswert unmittelbar anzeigt.

#### Laufende Bosslogik

Die zentrale Bosslogik läuft im Event FollowPlayer, das durch den zuvor gesetzten Timer in kurzen Intervallen wiederholt ausgeführt wird und damit permanent aktiv ist. Zu Beginn erfolgt die Abfrage, ob Current Health Boss den Wert 0 erreicht hat. Wenn diese Bedingung erfüllt ist, wird das Event Death ausgeführt. Im Death-Event wird über einen Cast zum AI Controller zuerst die Bewegung gestoppt und anschließend die Todesanimation abgespielt, sodass der Boss aus der aktiven Kampfsteuerung sauber herausgenommen wird.

Falls der Boss noch lebt, folgt die Abfrage von Can Shoot Projectile. Ist diese Bedingung false, nutzt der Boss AI Move To und bewegt sich mit einem Acceptance Radius von 250 in Richtung Spielerposition. Sobald der Boss den Zielbereich erreicht, wird geprüft, ob Can Punch aktiv ist. Wenn ja, wird Can Punch zunächst auf false gesetzt, das Array Hit Actors This Swing geleert und die Schlaganimation abgespielt, damit der Nahkampfzyklus mit einem definierten Ausgangszustand startet.

Für das aktive Trefferfenster wird nach einem kurzen Delay ein Set Timer by Function Name gestartet, der HitDetectBoss in einer Schleife aufruft. Nach einer weiteren kurzen Verzögerung wird dieser Funktionstimer wieder beendet, damit die Trefferprüfung nicht dauerhaft weiterläuft. Danach wird der Animationsmodus auf den normalen Bewegungszustand zurückgesetzt und Can Punch wieder auf true gesetzt, wodurch der Boss für den nächsten Nahkampfanlauf erneut freigegeben ist.

In HitDetectBoss selbst wird analog zur Player-Logik ein Knochen des Boss-Meshes als Ausgangspunkt verwendet und über Sphere Trace for Objects mit einem Radius von 200 die Trefferprüfung durchgeführt. Dabei wird das Array Hit Actors This Swing verwendet, sodass ein Ziel pro Schlag nur einmal verarbeitet wird. Anschließend wird geprüft, ob der getroffene Actor den Tag Player besitzt und ob das Interface BPI_Attack implementiert ist. Trifft beides zu, wird HitReaction aufgerufen, wodurch der Spieler 10 Schaden erhält.

Ist Can Shoot Projectile dagegen true, stoppt der Boss über den AI Controller zuerst die Bewegung, führt anschließend das Event WhatRangedAttack aus und setzt Can Punch wieder auf true.

#### Fernkampfentscheidung über WhatRangedAttack

Das Event WhatRangedAttack steuert, welche Fernkampfvariante im nächsten Zyklus ausgeführt wird. Zu Beginn wird ein Zufallswert zwischen 0 und 1 erzeugt und in Random Ranged Attack gespeichert. Anschließend entscheidet eine Abfrage mit dem Schwellenwert 0,3 zwischen der Homing-Variante und der normalen Projektilvariante.

Zur Ablaufkontrolle wird Do Once verwendet. Dadurch wird verhindert, dass derselbe Angriffszweig innerhalb eines Zyklus mehrfach startet. Über die Variable Next Is Reset wird gesteuert, wann Do Once wieder freigegeben wird. Die Cooldown-Rücksetzung nach der Schusssequenz erfolgt über das Event WaitUntilShotsFinished, das den Abschluss der Projektilserie überwacht und danach Can Shoot Projectile sowie Next Is Reset in den nächsten Zustand überführt.

#### Shoot und shootNext

Das Event Shoot initialisiert die eigentliche Schusssequenz. Dafür wird Shoot Index auf 0 gesetzt und ein wiederholt laufender Set Timer by Event mit einem Intervall von 1,0 Sekunden gestartet. Dieser Timer ruft shootNext periodisch auf.

In shootNext wird zuerst geprüft, ob der aktuelle Shoot Index noch innerhalb der verfügbaren Projektil-Arrays liegt. Für die normale Variante erfolgt die Prüfung gegen die Länge von Spawned Projectiles, für die Homing-Variante gegen die Länge von Spawned Homing Projectiles. Solange gültige Einträge vorhanden sind, wird die Sequenz fortgesetzt und ein weiterer Schuss ausgeführt.

Bei Random Ranged Attack kleiner oder gleich 0,3 wird die Homing-Variante verwendet. Da in diesem Modus nur ein einzelnes Homing-Projektil gespawnt wird, wird dieses mit festem Index 0 aus Spawned Homing Projectiles geholt und über Fire ausgelöst.

Bei der normalen Variante wird das Projektil über Spawned Projectiles mit Shoot Index adressiert. Zusätzlich wird Target Actor auf Player Ref gesetzt und abhängig vom Sprint-Zustand des Spielers ein geeigneter Zielpunkt berechnet. Danach wird Fire ausgeführt und Shoot Index um 1 erhöht.

Wenn keine weiteren gültigen Array-Einträge mehr vorhanden sind, wird der Timer über Clear and Invalidate Timer by Handle gestoppt, damit shootNext nicht weiterläuft.

#### WaitUntilShotsFinished

WaitUntilShotsFinished wird nach der normalen Schusssequenz ausgeführt und prüft, ob alle geplanten Schüsse bereits verarbeitet wurden. Dafür wird Length von Spawned Projectiles mit Shoot Index verglichen. Solange Length größer als Shoot Index ist, sind noch Schüsse offen. In diesem Fall wird die Prüfung über Set Timer by Event in kurzen Intervallen von 0,1 Sekunden erneut ausgeführt, sodass der Abschlusszustand nicht über einen festen Zeitpunkt, sondern über die tatsächliche Abarbeitung der Schussserie bestimmt wird.

Sobald die Bedingung nicht mehr erfüllt ist, gilt die Schussserie als abgeschlossen. Danach wird Can Shoot Projectile zunächst auf false gesetzt und der Cooldown gestartet. Nach einem Delay von 10,0 Sekunden wird Can Shoot Projectile wieder auf true gesetzt und Next Is Reset auf true gesetzt, damit der nächste Fernkampfzyklus wieder freigegeben ist und Do Once erneut korrekt zurückgesetzt werden kann.

#### SpawnProjectileAtSocket und SpawnHoming

SpawnProjectileAtSocket erzeugt die normale Projektilserie. Zuerst werden Spawned Projectiles und Spawn Points geleert. Danach werden die verfügbaren Spawn-Komponenten in Spawn Points eingetragen. Die Anzahl der zu spawnenden Projektile wird dynamisch über den Boss-Lebenszustand bestimmt. Liegt Current Health Boss bei höchstens der Hälfte von Max Health Boss, wird Spawn Count auf 5 gesetzt, sonst auf 3.

Für die Schleife wird Spawn Count minus 1 als Last Index verwendet, damit der Arrayzugriff über Get korrekt zur Anzahl der Spawn Points passt. In jedem Schleifendurchlauf wird über den Transform des jeweiligen Spawn Points ein BP Projectile erzeugt und in Spawned Projectiles gespeichert.

SpawnHoming erzeugt die Homing-Variante. Dafür wird Spawned Homing Projectiles geleert, Shoot Index auf 0 gesetzt und ein BP Homing Projectile am definierten Spawnpunkt erzeugt. Das erzeugte Projektil wird in Spawned Homing Projectiles gespeichert, als Referenz gesetzt und mit der Boss-Referenz sowie der Zielkomponente des Spielers initialisiert.

#### Zielpunktberechnung mit GetPlayerLocation

GetPlayerLocation und GetPlayerSprintingLocation berechnen den Zielpunkt für die normale Schussvariante. Beide Events lesen zunächst Position und Geschwindigkeit des Spielers aus und berechnen über Vector Length den aktuellen Speed-Wert. Wenn der Spieler nahezu stillsteht, wird direkt die aktuelle Spielerposition als Zielpunkt verwendet.

Bewegt sich der Spieler, wird aus der Bewegungsrichtung ein Vorhaltepunkt berechnet. Dazu wird der Geschwindigkeitsvektor normalisiert und auf die Spielerposition addiert. In GetPlayerLocation wird mit einem Faktor von 200 gerechnet, in GetPlayerSprintingLocation mit 400. Dadurch wird bei Sprint ein weiter vorausliegender Zielpunkt verwendet, was die Treffergenauigkeit gegen schnelle Bewegung erhöht.

#### Logik des normalen BP_Projectile

Die zentrale Fluglogik startet im Event Fire. Zu Beginn wird geprüft, ob Target Actor gültig ist. Nur wenn diese Referenz vorhanden ist, wird die Zielrichtung berechnet.

Danach entscheidet die Variable Use Target Point über die Art der Richtungsberechnung. Wenn Use Target Point aktiv ist, wird aus Target Point minus aktueller Projektilposition der Richtungsvektor erzeugt. Andernfalls wird die Richtung über Zielposition des Target Actor minus aktueller Projektilposition berechnet.

Der resultierende Richtungsvektor wird normalisiert, mit dem Wert Speed multipliziert und anschließend als Velocity in der Projectile Movement Component gesetzt. Dadurch fliegt das Projektil mit konstanter Geschwindigkeit entlang des berechneten Zielvektors.

Die Trefferverarbeitung erfolgt über On Component Begin Overlap der Kollisionskomponente. Dabei wird geprüft, ob Other Actor dem Player Character entspricht. Nur in diesem Fall wird der Schadenspfad ausgeführt.

Zur Absicherung gegen Mehrfachtreffer verwendet die Logik Do Once. Danach wird Apply Damage mit den Werten Damaged Actor gleich Player Character, Base Damage gleich Damage, Event Instigator über Get Instigator Controller und Damage Causer gleich Self ausgeführt. Unmittelbar nach dem Schaden wird das Projektil über Destroy Actor entfernt.

Zusätzlich enthält die Blueprint-Logik eine zeitgesteuerte Selbstzerstörung nach 10 Sekunden. Dadurch bleiben keine Projektile dauerhaft in der Szene, falls kein Treffer zustande kommt.

#### Logik des BP_HomingProjectile

Die Fire-Funktion des BP_HomingProjectile ist im Kern identisch zur Fire-Funktion des normalen BP_Projectile. Der Unterschied liegt nicht in der Grundberechnung der Flugbewegung, sondern in der Konfiguration der Projectile Movement Component.

Für das Homing-Verhalten wird in den Details der Projectile Movement Component die Einstellung Is Homing Projectile aktiviert. Damit folgt das Projektil nicht nur einer einmal berechneten Startbahn, sondern richtet sich während des Fluges laufend an der gesetzten Homing Target Component aus.

Im Event On Component Begin Overlap wird zunächst geprüft, ob der überlappte Actor den Tag Player besitzt. Danach wird über den Player-Character der aktuelle Parry-Zustand ausgelesen und gemeinsam mit der Variable Reflected ausgewertet.

Aus dieser Prüfung entstehen zwei Pfade. Im normalen Trefferpfad wird Apply Damage auf den Spieler ausgeführt und das Projektil anschließend mit Destroy Actor entfernt. Im Reflektionspfad wird über Do Once eine Mehrfachauslösung verhindert, danach die Boss-Instanz über Get All Actors of Class ermittelt, Boss Payback ausgeführt und das Projektil ebenfalls zerstört.

Zusätzlich enthält BP_HomingProjectile das Custom Event Reflect. Dabei wird Reflected auf true gesetzt und die Homing Target Component auf die Capsule Component des Boss umgestellt. Dadurch wechselt das Ziel nach erfolgreicher Parry-Reaktion vom Spieler auf den Boss.
