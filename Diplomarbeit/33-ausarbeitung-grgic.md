# Teilaufgabe Schüler Grgic
\textauthor{Grgic}

## Theorie

### Warum Unreal Engine gegenüber anderen Engines im Bereich Grafik & Rendering wählen?

#### Allgemein

***Allgemeine Ausrichtung von Unreal Engine***

Unreal Engine ist von Grund auf für High-End-Grafik ausgelegt. Der Fokus liegt auf realistischer Lichtberechnung und physikalisch korrekter Darstellung statt auf vereinfachtem "Fake Lighting". Die Standard-Workflows orientieren sich stark an professionellen Film-, VFX- und Architektur-Pipelines. Ziel ist eine möglichst hohe visuelle Qualität bei gleichzeitig geringem manuellem Optimierungsaufwand.

***Gegensatz zu Unity***

Unity ist stärker auf Performance, mobile Plattformen und breite Hardware-Unterstützung ausgerichtet. Hochwertige Grafik ist zwar möglich, erfordert jedoch mehr Konfigurationsaufwand, mehr Erfahrung und zusätzliche Arbeitsschritte. Für dieses Projekt mit einer kleinen, überschaubaren Spielwelt ist diese mobile Optimierung nicht entscheidend.

#### Photorealismus & Realismus

***Unreal Engine***

Physikalisch basiertes Rendering (PBR) ist in Unreal Engine standardmäßig aktiv. Materialien reagieren dadurch realistisch auf Eigenschaften wie:

* Licht
* Rauheit
* Metallizität

Dadurch lassen sich glaubwürdige Oberflächen auch ohne tiefgehende Shader-Kenntnisse umsetzen. Bereits mit den Standardwerkzeugen der Engine sind hochwertige Ergebnisse möglich.

***Vergleich zu Unity***

Unity kann ebenfalls photorealistische Ergebnisse liefern, dies ist jedoch vor allem mit der High Definition Render Pipeline (HDRP) praktikabel. Dafür sind in der Regel nötig:

* höherer Konfigurationsaufwand
* detaillierte Shader-Anpassungen
* zusätzliche manuelle Feinarbeit

Im Vergleich dazu liefert Unreal Engine ähnliche oder bessere Ergebnisse schneller und konsistenter.

#### Nanite - Virtuelle Geometrie

***Unreal Engine***

Nanite ermöglicht die Verwendung extrem hochauflösender Modelle mit Millionen bis Milliarden Polygonen. Die Engine passt die Detailstufe automatisch an die aktuelle Ansicht an. Eine manuelle Erstellung von LOD-Stufen entfällt. Das reduziert Entwicklungszeit, Fehleranfälligkeit und Asset-Aufwand erheblich, was besonders für kleine Teams ein Vorteil ist.

Nanite eignet sich besonders für:

* Scan-Daten
* Architekturvisualisierungen
* detailreiche Spielwelten

***Vergleich zu Unity***

Unity verwendet ein klassisches LOD-System, bei dem Detailstufen manuell erstellt werden müssen. Die Performance hängt dadurch stärker von der Asset-Optimierung ab. Ein direkt vergleichbares System wie Nanite ist in Unity nicht in gleicher Form vorhanden.

#### Lumen - Dynamische Global Illumination

***Unreal Engine***

Mit Lumen berechnet Unreal Engine globale Beleuchtung und Reflexionen vollständig in Echtzeit. Das Licht reagiert dynamisch auf:

* bewegte Objekte
* Zerstörung
* Tageszeitwechsel

Klassisches Light Baking ist nicht zwingend notwendig. Szenen wirken dadurch lebendiger und konsistenter, während der Iterationsaufwand im Leveldesign sinkt.

***Vergleich zu Unity***

Unity setzt häufig auf vorab berechnetes Light Baking. Bei Änderungen am Level muss das Licht oft neu berechnet werden. Echtzeit-Global-Illumination ist nur eingeschränkt verfügbar und kann performanceintensiv sein.

Lumen reduziert dadurch:

* Zeitaufwand
* Speicherbedarf
* Iterationsaufwand

#### Post-Processing & Bildqualität

***Unreal Engine***

Unreal Engine bietet eine integrierte Post-Processing-Pipeline mit Effekten wie:

* Bloom (Überstrahlen heller Lichtquellen)
* Motion Blur (Bewegungsunschärfe)
* Depth of Field (Tiefenunschärfe)
* Film Grain (Simulation analoger Filmkörnung)

Post-Processing beschreibt die digitale Nachbearbeitung des gerenderten Bildes zur Verbesserung von Atmosphäre und Bildwirkung. Die Effekte sind über Post-Process-Volumes steuerbar und ermöglichen einen konsistenten, filmischen Look.

***Vergleich zu Unity***

In Unity werden Post-Processing-Effekte häufig über zusätzliche Pakete integriert. Die Abstimmung ist komplexer und erfordert mehr manuelle Konfiguration. In Unreal Engine lässt sich ein cineastischer Look meist schneller erreichen.

#### Workflow & Produktivität (grafikbezogen)

***Unreal Engine***

Unreal Engine bietet eine realitätsnahe Editor-Vorschau. Das sichtbare Ergebnis entspricht in der Regel dem finalen Spielbild ("What you see is what you get"). Änderungen an Licht, Materialien oder Geometrie sind sofort sichtbar, was iteratives Arbeiten deutlich beschleunigt.

***Vergleich zu Unity***

In Unity sind häufiger Test-Builds notwendig. Das Endergebnis hängt stärker von Zielplattform, Render-Pipeline und Build-Einstellungen ab, wodurch der Feedback-Zyklus langsamer sein kann.

\newpage

### Warum Unreal Engine im Bereich Programmierung & Blueprints wählen?

#### Grundidee der Blueprints

Unreal Engine bietet ein vollständig integriertes visuelles Skripting-System. Die Spiellogik wird über node-basierte Graphen abgebildet. Funktionen, Events und Variablen sind grafisch darstellbar, wodurch auf klassischen Textcode teilweise verzichtet werden kann. Der Fokus liegt auf Verständlichkeit, Übersichtlichkeit und logischem Aufbau statt auf Syntax.

#### Programmieren ohne klassischen Code

Blueprints sind ein zentraler Bestandteil der Unreal Engine und nahtlos in alle Systeme integriert.

**Vorteile:**

* kein zwingendes Vorwissen in C++ erforderlich
* Einstieg auch ohne tiefe Programmierkenntnisse möglich
* Fehler sind oft leichter nachvollziehbar als bei reinem Textcode
* Logik ist visuell gut lesbar

***Vergleich zu Unity***

Unity verwendet primär C#-Skripte. Visuelles Skripting ist vorhanden, aber weniger tief in die Engine-Workflows integriert.

#### Node-System & Logikaufbau

***Unreal Engine***

Nodes repräsentieren:

* Funktionen
* Events
* Bedingungen
* Schleifen

Dabei wird klar zwischen Ablaufsteuerung (Execution Flow) und Datenfluss (Variablen) unterschieden. Auch komplexe Logiken lassen sich damit ohne lange Code-Dateien strukturieren. Besonders geeignet ist dieses System für:

* Gameplay-Logik
* Benutzeroberflächen
* Interaktionen
* Trigger-Systeme

***Vergleich zu Unity***

In Unity ist Logik primär textbasiert. Visuelle Systeme sind meist Zusatztools und bieten häufig weniger direkte Übersicht über den Ablauf.

#### Ideal für Anfänger & Designer

Unreal Engine erleichtert den Einstieg für Anfänger erheblich. Designer können Gameplay-Elemente selbst umsetzen und Anpassungen ohne direkten Eingriff von Programmierern vornehmen. Das fördert interdisziplinäres Arbeiten und reduziert Abhängigkeiten im Team.

#### Schnelles Prototyping

***Unreal Engine***

Gameplay-Ideen lassen sich schnell umsetzen. Änderungen sind sofort testbar und erfordern oft kein langes Kompilieren. Der iterative Entwicklungsprozess wird dadurch beschleunigt.

***Vergleich zu Unity***

In Unity ist nach Codeänderungen häufig eine erneute Kompilierung nötig, wodurch Testzyklen länger werden.

#### Kombination aus Blueprints & C++

***Unreal Engine***

Unreal Engine erlaubt die gezielte Kombination aus C++ und Blueprints. Grundlogik kann in C++ implementiert werden, während Feinabstimmungen in Blueprints erfolgen. Performancekritische Bereiche lassen sich damit gezielt optimieren.

***Vergleich zu Unity***

Unity setzt primär auf C# und bietet weniger klare Trennung zwischen Low-Level-Logik und visuellem Gameplay-Scripting.

#### Änderungen in Echtzeit sichtbar

***Unreal Engine***

Änderungen an Blueprints sind unmittelbar im Spiel testbar. Zusätzliche Neustarts oder Builds sind oft nicht nötig, was Debugging und Feinschliff erleichtert.

***Vergleich zu Unity***

In Unity ist häufiges Stoppen und Neustarten des Play-Modus notwendig, was den Feedback-Zyklus verlangsamt.

### Warum Unreal Engine gegenüber anderen Engines im Bereich Game Development wählen?

#### Allgemeine Einordnung

Unreal Engine ist heute nicht nur eine Spiele-Engine, sondern eine umfassende Echtzeit-3D-Plattform. Der Schwerpunkt liegt auf hochwertiger visueller Darstellung, Simulationen und interaktiven Echtzeitsystemen. Unity wird ebenfalls in vielen Bereichen eingesetzt, ist aber stärker im mobilen und leichtgewichtigen Bereich verbreitet. Unreal Engine ist klar auf High-End-Visualisierung und hohe Bildqualität ausgerichtet.

#### Game Development

***Unreal Engine***

Im Game Development liegt der Fokus von Unreal Engine besonders auf High-End-PC- und Konsolenspielen. Das zeigt sich in realistischer Grafik, großen Spielwelten und modernen Technologien. Features wie Nanite, Lumen und Blueprints eignen sich besonders für atmosphärische Spiele und Projekte mit hohem Qualitätsanspruch.

***Vergleich zu Unity***

Unity ist im mobilen Bereich stark verbreitet, da geringere Hardwareanforderungen und breite Plattformunterstützung möglich sind. Für grafisch sehr anspruchsvolle Projekte ist jedoch oft zusätzlicher Optimierungsaufwand nötig.

#### Architekturvisualisierung

Unreal Engine wird häufig für Echtzeit-Architekturvisualisierungen und interaktive Gebäudebegehungen eingesetzt. Im Vergleich zu statischen Renderbildern bietet Unreal Engine eine deutlich realistischere und interaktive Darstellung.

**Vorteile:**

* realistische Lichtsimulation
* Interaktion statt statischer Darstellung
* physikalisch korrektes Materialverhalten
* Echtzeit-Änderungen von Tageszeit, Beleuchtung und Materialien

Genutzt wird Unreal Engine unter anderem von:

* Architekturbüros
* Bauunternehmen
* Immobilienentwicklern

#### Film & Animation (Virtual Production)

***Unreal Engine***

Unreal Engine spielt eine zentrale Rolle in der Virtual Production. LED-Walls und Echtzeit-Hintergründe ersetzen dabei zunehmend klassische Greenscreen-Techniken.

**Vorteile:**

* Beleuchtung passt sich direkt der virtuellen Umgebung an
* geringerer Postproduktionsaufwand
* kosteneffizientere Produktionsprozesse
* schnellere Entscheidungsfindung am Set
* Regie und Team sehen das Ergebnis direkt während der Aufnahme

***Vergleich zu klassischen Pipelines***

Traditionell werden Szenen vor Greenscreen aufgenommen und Hintergründe erst in der Postproduktion ergänzt. Mit Unreal Engine können diese Schritte bereits in Echtzeit während der Aufnahme stattfinden.

#### Simulationen

Unreal Engine wird für unterschiedliche Simulationsarten eingesetzt, zum Beispiel physikbasierte Trainingsumgebungen sowie Sicherheits- und Gefahrenszenarien. Typische Einsatzbereiche sind Industrie, Forschung, Ausbildung und militärische Anwendungen.

**Vorteile:**

* Echtzeit-Feedback
* realistische Umgebungen
* kombinierbar mit KI-Systemen

#### VR / AR

Unreal Engine bietet starke Unterstützung für Virtual Reality und Augmented Reality. Die hohe Bildqualität ist wichtig für Immersion und Realismus. Typische Anwendungsbereiche sind Trainingssimulationen, medizinische Anwendungen und Produktpräsentationen. Die hohe grafische Qualität bringt allerdings höhere Hardwareanforderungen mit sich.

#### Automobilindustrie

Unreal Engine wird auch in der Automobilindustrie eingesetzt, etwa für Fahrzeugvisualisierungen, Design-Reviews und virtuelle Showrooms. In der Praxis ermöglicht das schnellere Entwicklungszyklen, bessere Entscheidungsgrundlagen und eine Reduktion physischer Prototypen.

**Vorteile:**

* realistische Materialien (Lack, Glas, Metall)
* Echtzeit-Anpassungen von Farben, Innenausstattung und Beleuchtung

#### Digitale Zwillinge

Unreal Engine wird zur Erstellung digitaler Zwillinge realer Systeme, Prozesse oder Objekte verwendet. Einsatzgebiete sind unter anderem Smart Cities, Industrieanlagen und Verkehrsmodelle. Diese digitalen Zwillinge verbinden:

* Echtzeitdaten
* 3D-Visualisierung
* Simulation

Der Mehrwert liegt in der Analyse komplexer Systeme, der Vorhersage von Verhalten und der Optimierung realer Prozesse.

\newpage

## Praktische Arbeit

### Übersicht

In diesem Kapitel wird die praktische Umsetzung in Unreal Engine beschrieben. Der Schwerpunkt liegt auf der Architektur des Spiels und den wichtigsten Gameplay-Systemen.

Das Spiel besteht aus mehreren zentralen Komponenten: dem Player-System, der Boss-KI, dem Kampfsystem und verschiedenen Projektilmechaniken. Diese Systeme greifen ineinander, um einen interaktiven und spielerisch fordernden Bosskampf zu ermöglichen.

### Architektur des Spiels

Die wichtigsten Blueprints sind:

* `BP_FirstPersonCharacter`
* `BP_Boss`
* `BP_Projectile`
* `BP_HomingProjectile`

Die Klassen haben klar getrennte Aufgaben. `BP_FirstPersonCharacter` steuert Bewegung, Kamera, Angriff, Stamina und Parry-Logik. `BP_Boss` verwaltet Boss-Leben, Angriffsabläufe und das Spawnen der Projektile. Die Projektil-Blueprints übernehmen Flugverhalten, Kollision und Spezialverhalten wie Homing und Reflexion.

**Bildhinweis:** Übersichts-Screenshot des Blueprint-Ordners oder der wichtigsten Klassen im Content Browser, damit die Systemstruktur sofort erkennbar ist.

### Player-System

#### Bewegung und Grundkonfiguration

Der Spieler wird über `BP_FirstPersonCharacter` gesteuert. Die Kamera ist an die Blickrichtung gekoppelt, sodass sich die Figur beim horizontalen Drehen mitorientiert. Das eigene Character-Mesh ist für die First-Person-Kamera unsichtbar geschaltet, damit keine störenden Körperteile im Sichtfeld auftauchen. Zusätzlich wurden Bewegungswerte wie Laufgeschwindigkeit und Grundbeschleunigung auf das Kampfsystem abgestimmt.

**Bildhinweis:** Screenshot der Kamera- und Movement-Einstellungen in `BP_FirstPersonCharacter` (Camera Component, Mesh-Visibility, Rotation/Movement Settings).

#### Dodge-System

Das Ausweichsystem (Dodge) basiert auf der Unreal-Engine-Funktion **Launch Character** und ist direkt mit dem Stamina-System verbunden.

* Pro Dodge werden **20 Stamina** von insgesamt 100 verbraucht.
* Die Boolean-Variable **isDodging** verhindert Spam und setzt einen Cooldown von 1 Sekunde.
* Während der Dodge-Aktion ist kein erneuter Dodge möglich.

Damit ist das Ausweichen ein bewusst eingesetztes Verteidigungswerkzeug und keine dauerhaft verfügbare Bewegungstechnik.

**Bildhinweis:** Blueprint-Abschnitt mit `InputAction Dodge`, `Launch Character`, Stamina-Abzug und `isDodging`-Cooldown.

#### Angriffssystem

Der Angriff wird über ein Action Mapping in den Projekteinstellungen ausgelöst (`InputAction Attack` auf linker Maustaste). Beim Drücken läuft folgender Ablauf ab:

1. **isAttacking** wird auf `true` gesetzt, damit keine überlappenden Angriffe starten.
2. Das Array **hitActorsThisSwing** wird geleert, damit pro Schlag jeder Actor nur einmal Schaden erhält.
3. Die Schlaganimation wird abgespielt.
4. Pro Schlag werden **10 Stamina** abgezogen.
5. Nach **1,0 s** wird **isAttacking** wieder auf `false` gesetzt.
6. Der **Animation Mode** wird zurückgesetzt, damit die Figur nicht in der Attack-Animation hängen bleibt.
7. Die Stamina-Regeneration startet erst nach weiteren **1,5 s**.

Diese Reihenfolge stellt sicher, dass das Kampfsystem kontrolliert, fair und gut ausbalancierbar bleibt.

**Bildhinweis:** Blueprint-Flow von `InputAction Attack` mit `isAttacking`, `Clear hitActorsThisSwing`, `Play Animation`, Delay und `Set Animation Mode`.

#### Hit-Detection (Schlag-Erkennung)

Die Treffererkennung erfolgt über die Funktion **Hitdetect**. Dafür wird in der Animation ein Knochen ausgewählt, um den während aktiver Angriffsframes eine Hitbox erzeugt wird.

* Beispiel: aktive Frames zwischen 20 und 35.
* Hitbox-Typ: unsichtbare **Sphere Collision**.
* Standardradius: 20 cm (frei anpassbar).
* Unreal Engine verwendet Zentimeter, daher gilt: Radius 1 = 1 cm.

Ablauf der Trefferprüfung:

1. Ein **Branch** (if-Abfrage) prüft, ob die Sphere einen Treffer meldet.
2. Über **Break Hit Result** wird der getroffene **Actor** ausgelesen.
3. Es wird geprüft, ob der Actor bereits in **hitActorsThisSwing** enthalten ist.
4. Falls nicht enthalten, wird er hinzugefügt und weiter verarbeitet.
5. Danach folgt die Tag-Prüfung auf **Enemy**.
6. Bei **Enemy** wird geprüft, ob das Interface **BPI_Attack** implementiert ist.
7. Wenn ja, wird **HitReaction** ausgelöst.

Damit wird verhindert, dass ein Gegner innerhalb eines einzelnen Schlages mehrfach Schaden erhält.

**Bildhinweis:** Blueprint der Funktion `Hitdetect` mit Sphere-Trace/Collision, `Break Hit Result`, Array-Prüfung (`hitActorsThisSwing`) und Interface-Check (`BPI_Attack`).

#### Parry und Projektil-Reflexion

Zusätzlich gibt es beim Angreifen ein kurzes Parry-Fenster:

* Beim Drücken von `InputAction Attack` wird **parryActive** für **0,5 s** auf `true` gesetzt.
* Trifft der Spieler in dieser Zeit keinen `Enemy`, wird geprüft, ob ein reflektierbares Projektil getroffen wurde.
* Der getroffene Actor muss dafür den Tag **Reflectable** besitzen.
* Danach wird **Cast To BP_HomingProjectile** ausgeführt.
* Bei erfolgreichem Cast wird das **Reflect**-Event aufgerufen.

Der Cast ist notwendig, damit nur Projektile mit passender Klasse reflektiert werden und die projektilspezifische Logik sicher verfügbar ist.

**Bildhinweis:** Blueprint-Screenshot mit `parryActive`, Tag-Check `Reflectable`, `Cast To BP_HomingProjectile` und `Reflect`-Event.

#### Zwischenfazit zum Player-System

Das Player-System kombiniert Bewegung, Ressourcenkontrolle (Stamina), Nahkampf und defensive Mechaniken (Dodge/Parry) zu einem geschlossenen Regelwerk. Durch Cooldowns, Zustandsvariablen und klare Trefferlogik entsteht ein System, das sowohl spielbar als auch technisch nachvollziehbar bleibt.
