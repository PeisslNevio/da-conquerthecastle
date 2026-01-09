# Teilaufgabe Schüler Grgic
\textauthor{Grgic}

## Theorie

### Warum Unreal Engine gegenüber anderen Engines wählen?

#### Grafik & Renddering

***Allgemeine Ausrichtung von Unreal Engine***

Unreal Engine ist von Grund auf auf High-End-Grafik ausgelegt und der Fokus bezieht sich mehr auf realistische Lichtberechnung statt "Fake-Lighting". Die Standard Workflows orientieren sich an Film- und VFX-Pipelines sowie das Ziel von Unreal Engine ist maximale Visuelle Qualität bei möglichst wenig manueller Optimierung.

***Gegensatz zu Unity***

Unity ist stärker auf Performance, Mobile und breite Plattformen optimiert, wobei dies nicht relevant für unsere kleine Welt im Projekt ist. Hochwertige Grafik erfordert dort mehr Setup, Erfahrung und Zusatzarbeit.

#### Photorealismus & Realismus

***Unreal Engine***

Physikalisch basiertes Rendering(PBR) ist standardmäßig aktiv und Materialien reagieren realistisch auf:
  * Licht
  * Rauheit
  * Metallizität

Durch Unreal Engine kann man sehr glaubwürdige Oberflächen ohne Shader-Spezialwissen darstellen und auch Out-of-the-box reallistische Ergebnisse darbringen.

***Vergleich zu Unity***

Unity kann photorealistisch sein, aber es funkzionirt nur mit:
  * HDRP (High Definition Render Pipeline)
  * Höhereren Konfigurationsaufwand
  * mehr manuellen Feinarbeiten an Shadern

Im Vergleich liefert Unreal Engine veergleichbare Ergebnisse schneller und konsistenter

#### Nanite - Virtuelle Geometrie

***Unreal Engine***

Nanite ermöglicht extrem hochauflösende Modelle und ermöglicht auch Millionen bis Milliarden von Polygonen, welches bei kleineren Modellen(auf Polygonen bezogen) bessere Performance darbieten kann. Nanite reduziert auch die Entwicklungszeit, Fehleranfälligkeit und sowie den Asset-Aufwand, was für kleine Teams einen Vorteil bietet. Es ist keine manuelle LOD-Erstellung nötig und Unreal Engine unterscheidet automatisch welche Geometrie sichtbar ist und welche Detailstufe benötigt wird. Dies ist Ideal für:
  * Scan-Daten
  * Architekturszenen
  * Detailreiche Spielwelen

***Vergleich zu Unity***

Unity besitz nur ein klassisches LOD-System und sowie müssen LODs manuell erstellt werden, sowie ist dann die Performance stark von der Optimierung abhängig. Unity besitz auch Nanite.

#### Lumen - Dynamische Global Illumination

***UNreal Engine***

Unreal Engine brechnet in Echtzeit die gloable Illumination und Refletionen, sowie reagiert dieses Licht dynamisch auf:
  * bewegte Objekte
  * Zertörung
  * Tageszeitwechsel

In Unreal Engine ist kein Light-baking benötigt, was komplexes Licht vorrechnet von statischen Objekten und es speichert in deren "lightmaps" für performance. Dadurch wirken die Szenen natürlicher, lebendiger und sowohl auch konsistenter.

***Vergleich zu Unity***

Verwendet Light-Baking und jedes mal wenn das Level geändert wird, wird ein neues Baking benötigt. Das Echtzeit-GI in Unity ist eingeschränkt und performance-intensiv. 

Lumen erspart:
  * Zeit
  * Speicher
  * Iterationsaufwand

#### Post-Processing & Bildqualität

***Unreal Engine***

In Unreal Engine sind hochwerige Effekte direkt integriert:
  * Bloom, lässt helle Lichtquellen überstrahlen
  * Motion Blur, erzeugt eine verschwommene Darstellung von schnellen Objekten oder der Kamera
  * Depth of Field, simuliert eine echte Kamera was einen Teil der Szene scharf und den Rest unscharf darstellt
  * Film Grain, imitiert echtes analoges Filmaterial

Post-Processing, ist eine digitale Nachbearbeitung des fertigen Bildes, um Grafik und Atmospähre zu verbessern. Dies ist über Volumes steuerbar. Es gibt einen einheitlichen Look über die gesamte Szene und es gibt einen Filmischen Gesamteindruck

***Vergleich zu Unity***

In Unity ist Post-Processing oft über Packages verfügbar und es ist mehr manuelle Abstimmung nötig. Wo in UNreal ein Cinematik Look schneller erreichbar ist und weniger technische Hürden sind.

#### Workflow & Produktivität (Grafikbezogen)

***Unreal Engine***

Unreal Engine besitzt eine sehr gute Vorschau, das bedeutet was man im Editor sieht ist meistens auch das Endergebnis. "What you see is what you get". Sowie Änderungen an Licht Einstellungen oder Materialien an Modellen sind sofort Sichtbar und es ist optimal für Iteratives Arbeiten und Visuelles Feintuning.

***Vergleich mit Unity***

 In Unity sind mer Test-Builds nötig und das Ergebnis hängt stärker ab von:
  * Zielplattform
  * Render Pipeline
  * Build-Einstellungen


---
## Praktische Arbeit
