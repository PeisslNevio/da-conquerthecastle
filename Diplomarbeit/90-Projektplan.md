# Projekthandbuch
\textauthor{Peißl}

## Entwicklungsplan

### Projektauftrag

Diese Diplomarbeit beschäftigt sich mit der Entwicklung eines eigenständigen First-Person-Bosskampfs in der Unreal Engine 5. Das Ziel ist die Umsetzung eines vollständigen, spielbaren Szenarios, das aus einem selbst modellierten Bosscharakter, einem thematisch passenden Bossraum, den dazugehörigen Animationen sowie der notwendigen Spielmechanik besteht. Zudem gibt es am Anfang und am Ende kurze Cutscenes, um den Spieler in die Geschichte mit hinein zuziehen.

Diese Arbeit ist dadurch geprägt, dass zu Beginn keine technischen oder gestalterischen Grundlagen vorhanden sind. Weder Modelle, Animationen, Leveldesign noch Gameplay-Logik existieren. Die Herausforderung liegt darin, alle erforderlichen Komponenten – von der Modellierung über die Programmierung bis hin zur visuellen Gestaltung – eigenständig aufzubauen und zu einem funktionierenden Gesamtsystem zu verbinden.

Die Komplexität der Spielentwicklung kann man  grob in verschiedene Disziplinen aufteilen: 3D-Design, Animation, Engine-Workflow, Skripting, Soundintegration und Performanceoptimierung. Diese Fähigkeiten müssen in kurzer Zeit koordiniert werden. Gleichzeitig soll ein konsistenter visueller Stil gewahrt bleiben, und das Endprodukt muss technisch stabil und spielbar sein. Dieses Projekt bietet daher eine realitätsnahe Gelegenheit, professionelle Entwicklungsprozesse im Bereich Game Development praktisch umzusetzen.


#### Projektziele

- Erstellung eines vollständigen, funktionierenden Bosskampfes in First-Person-Perspektive  
- Modellierung eines Bosscharakters einschließlich Animationen  
- Gestaltung und Umsetzung des Bossraums im Low-Poly-Stil  
- Implementierung der Spielmechaniken (KI-Verhalten, Treffererkennung, Lebenssystem, Attacken, Kamera- und Spielersteuerung)  
- Entwicklung kurzer Cutscenes (Intro und Outro)  
- Sicherstellung eines konsistenten Designs und einer flüssigen Spielerfahrung  
- Dokumentation der technischen Entscheidungen, Workflows und Herausforderungen  

#### Nicht-Ziele bzw. nicht Inhalte

- Entwicklung eines vollständigen Spiels mit Story, mehreren Levels oder Open-World-Elementen  
- Erstellung einer komplexen Benutzeroberfläche über die nötigsten Spielmechaniken hinaus  
- Multiplayer-Funktionen oder Netzwerksynchronisation  
- Kommerzielle Veröffentlichung oder Marketing des Produktes  

#### Projektnutzen

Dieses Projekt bietet einen klaren fachlichen und pädagogischen Mehrwert. Die Umsetzung eines vollständigen Bosskampfs in der Unreal Engine 5 mit dreidimensionalen Modellen von Blender ermöglicht die verwendung von moderne Technologien, theoretisch so wie praktisch. Dadurch entsteht ein Kompetenzzuwachs in Bereichen wie 3D-Modellierung, Animation, Programmierung, Engine-Workflow und Projektorganisation – alles Fähigkeiten, die in der heutigen IT- und Medienwelt stark nachgefragt sind.

Gleichzeitig schafft das Projekt ein sichtbares, funktionierendes Endprodukt, das als Demonstrator für zukünftige Klassen und schulische Präsentationen eingesetzt werden kann. Der Nutzen liegt somit nicht nur beim Projektteam, sondern auch bei der Schule, die ein professionell wirkendes Showcase erhält. Zudem fördert das Projekt die Teamfähigkeit, das technische Problemlösen und das strukturierte Arbeiten über einen längeren Zeitraum hinweg. 

#### Projektauftraggeber/in

Diese Arbeit wurde von uns selbst vorgeschlagen und von der HTL Leoben angenommen.
Herr Prof. Kondert betreut diese Arbeit. 

Folgend sind die Kontaktdaten der HTL Leoben.

| **Feld**               | **Information**                           |
|------------------------|-------------------------------------------|
| **Name**               | HTL Leoben                                |
| **Adresse**            | Max Tendler-Straße 3, 8700 Leoben         |
| **URL**                | https://www.htl-leoben.at                 |
| **E-Mail**             | office@htl-leoben.at                      |
| **Ansprechpartner/in** | Christina Stroissnigg                     |
| **Telefon**            | +43 3842 44 888 0                         |
| **Typ**                | Fachhochschule                            |


#### Projekttermine

Hier werden die wichtigsten Meilensteine dokumentiert.

| Datum       | Meilenstein                               |
|------------:|:------------------------------------------|
| 20.09.2025  | Projektvorbereitung & Projektstart        |
| 30.09.2025  | Anforderungsanalyse & Konzept             |
| 20.10.2025  | Prototyp & Grundstruktur                  |
| 11.11.2025  | Zwischenpräsentation                      |
| 30.11.2025  | Implementierung Gegner & Gamelogik        |
| 20.12.2025  | Kampfsystem & UI                          |
| 30.12.2025  | Erstversion DA                            |
| 09.01.2026  | Feinschliff & Finale Tests                |
| 15.02.2026  | Spiel Abgeschlossen                       |
| 06.03.2026  | Endabgabe                                 |



#### Projektkosten

Hier ist eine Übersicht, wie viel unsere Diplomarbeit vorraussichtlich kosten wird.

| Kostenname  | Kostenart | Menge  | Preis   | Gesamtkosten | Deckung durch |
|:-------------|:---------:|:------:|--------:|-------------:|---------------|
| ChatGPT Abo     | Software  |  12 |   23.00 | 276.00      | Schüler       |
| 3D Assets | Software  |  1     |  30.93 | 30.93      | Schüler|
| DA-Schreiben | Druck     |  3     |   26.00 |  53.00      | Schüler       |

__Das Projekt kostet in Summe vorraussichtlich 359,93 Euro__. 



#### Projektrisiken

Hier ist unsere einschätzug von den möglichen Risiken sowie deren Wahrscheinlichkeiten.

| Risiko                                   | EW  | Auswirkungen                                                                 | Maßnahmen |
|:----------------------------------------:|:---:|:-----------------------------------------------------------------------------|:----------|
| Unterschätzung des technischen Aufwands   | 35% | Gameplay, Animationen oder Bosslogik werden später fertig als geplant       | Frühzeitige Prototypen, klare Meilensteine, regelmäßige Reviews |
| Probleme bei 3D-Modellierung oder Rigging | 25% | Bossmodell kann nicht rechtzeitig animiert oder ins Spiel integriert werden | Vereinfachung des Modells, frühzeitige Tests in UE5, Backup-Modell |
| Unreal Engine 5 Performance-/Kompatibilitätsprobleme | 20% | Ruckeln, Crashes, hohe Nacharbeit nötig                                      | Optimierung von Anfang an, Low-Poly konsequent einsetzen |
| Zeitmanagement- oder Ressourcenprobleme im Team | 30% | Verzögerungen, ungleich verteilte Aufgaben, Qualität leidet                  | Wochenplanung, klare Verantwortlichkeiten, Transparenz im Team |
| Fehler in der Game-Logik / KI            | 20% | Bosskampf wirkt unfertig oder ist nicht spielbar                             | Iteratives Testen, isolierte Logikmodule, Debugging-Sessions |
| Verlust von Dateien / Versionskonflikte  | 10% | Arbeitsfortschritt geht verloren                                              | Regelmäßige Backups, Nutzung von GitHub, klare Branch-Struktur |
| Ausfall wichtiger Software / Hardware    | 10% | Arbeiten stoppen, Deadlines verschieben sich                                 | Redundante Geräte, Cloud-Speicher, regelmäßige Updates |
| Umfang zu groß gewählt                   | 40% | Features werden nicht fertig, Qualität leidet                                 | Feature-Cut früh definieren, Fokus auf Kernmechanik |


### Projektorganisation

#### Projektbeteiligte

Hier werden alle Beteiligten an der Diplomarbeit samt Kontaktdaten gelistet.

| Vorname     | Nachname     | Organisation | Email      |Telefonnummer      |
|:------------|:-------------|:-------------|:------------------|:------------------|
| Christina    | Stroissnigg  | HTL Leoben   | office@htl-leoben.at  |03842448880|
| Uwe    | Kondert  | HTL Leoben   | kuw@O365.htl-leoben.at  |067761128667|
| Nevio       | Peißl      | HTL Leoben     | 211witb19@o365.htl-leoben.at    |068181749849|
| Rhys         | Schmiedpeter          | HTL Leoben          | 211witb23@o365.htl-leoben.at               |06641401336|
| Elias         | Grgic          | HTL Leoben          | 211witb06@o365.htl-leoben.at               |06644643590|



#### Projektrollen

Hier werden den Kontakten von oben konkrete Rollen zuewiesen.

| Projektrolle           | Rollenbeschreibung     | Name              |
|------------------------|------------------------|-------------------|
| Projektleiter | Verantwortlicher für Einhaltung des Projektrahmens | Nevio Peißl |
| Mitarbeiter | Ist an der DA beteiligt und muss seinen Teil erledigen | Rhys Schmiedpeter |
| Mitarbeiter | Ist an der DA beteiligt und muss seinen Teil erledigen | Elias Grgic |
| Auftraggeber | Auftraggeber der internen Diplomarbeit | Christina Stroissnigg |
| Betreuer | Schulischer Betreuer | Uwe Kondert |


In dieser Grafik werden die verschienen Rollen und deren Bezihungen dargestellt.

![Projektorganisationsdiagramm](img/projektorganisation.png){width=50%}


### Vorgehen bei Änderungen

Wenn sich innerhalb unserer Diplomarbeit etwas ändert, oder jemand einen Änderungsvorschlag hat muss dies zuerst mit dem Diplomarbeitsteam besprochen werden und darauf mit dem Betreuer. 
Betreuer und Teammitglieder werden darüber informiert und müssen auch dieser Änderung zustimmen. Alle Änderungen werden in der Projektdokumentation mit Datum festgehalten und ausführlich dokumentiert.

## Meilensteine

Der Begriff taucht im Projektmanagement sehr häufig auf. Meilensteine sind wichtige Punkte im Projektverlauf. Oft werden sie auch als Prüfpunkte bezeichnet.

Generell kann ein Meilenstein ein Ereignis sein, an dem

* etwas abgeschlossen ist,
* etwas begonnen wird oder
* über die weitere Vorgehensweise entschieden wird

Hier werden alle Meilensteine noch einmal mit Beschreibung aufgezählt:

### 2025-09-20: Projektvorbereitung & Projektstart

- Projekthandbuch begonnen und grundlegende Struktur festgelegt  
- Rollenverteilung innerhalb des Teams definiert  
- Projektumgebung eingerichtet (UE5, Blender, Git)  
- Erste Abstimmung über Stil, Umfang und technische Rahmenbedingungen  

### 2025-09-30: Anforderungsanalyse & Konzept

- Vollständige Beschreibung des Bossraums, Bosses und Kernspielmechaniken erstellt  
- Technisches Konzept für Animationen, KI, Leveldesign und Cutscenes ausgearbeitet  
- Risiken, Abgrenzungen und Projektziele definiert  
- Erste grobe Skizzen und Designideen dokumentiert  

### 2025-10-20: Prototyp & Grundstruktur

- Grundlegendes First-Person-Controller-System implementiert  
- Leerer Bossraum als Blockout aufgebaut  
- Pipeline für Import von 3D-Modellen getestet  
- Basislogik (Input, Bewegung, Kamera) lauffähig  

### 2025-11-11: Zwischenpräsentation

- Vorstellung des bisherigen Entwicklungsstands  
- Blockout-Bossraum, frühe Bossmodell-Version und erste Animationstests gezeigt  
- Feedback vom Betreuer eingeholt und weitere Schritte angepasst  

### 2025-11-30: Implementierung Gegner & Gamelogik

- Bossmodell vollständig fertiggestellt (inkl. Rigging und Animationen)  
- Grundlegende KI-Logiken implementiert (Bewegung, Attack-Muster, Phasenlogik)  
- Treffererkennung und Schadenssystem funktionsfähig  
- Basis für spätere Kampfmechaniken vorbereitet  

### 2025-12-20: Kampfsystem & UI

- Spielerangriffe, Block-/Ausweichmechaniken und Kollisionslogik abgeschlossen  
- UI für Lebensanzeige, Boss-Intro und Trefferfeedback implementiert  
- Kameraeffekte und visuelle Rückmeldungen integriert  
- Kampf in erster spielbarer Form funktionsfähig  

### 2025-12-30: Erstversion der Diplomarbeit

- Grobversion der schriftlichen DA erstellt  
- Alle Kapitel strukturiert und mit Platzhaltern für technische Inhalte gefüllt  
- Dokumententeile pro Teammitglied zusammengeführt  

### 2026-01-09: Feinschliff & Finale Tests

- KI-Verbesserungen, Bugfixes und Feintuning der Kampfmechaniken  
- Beleuchtung, Umgebungstexturen und Partikeleffekte finalisiert  
- Cutscenes (Intro/Outro) vollständig integriert  
- Alle Projektteile getestet und optimiert  

### 2026-02-15: Spiel abgeschlossen

- Finaler Bosskampf ist vollständig spielbar und stabil  
- Projektstände in Git sauber dokumentiert  
- Alle Deliverables abgeschlossen (Video, Screenshots, Präsentationsmaterial)  

### 2026-03-06: Endabgabe

- Diplomarbeit vollständig fertig, lektoriert und gebunden  
- Digitale Version hochgeladen  
- Evaluations- und Betreuungsprotokolle beigelegt  
- Projekt offiziell abgeschlossen  



#HIER WEITERMACHEN

## Anwendungsfälle

Hier beschreiben Sie die Anwendungsfälle (=UseCases) Ihrer Anwendung / Diplomarbeit. Dabei sollte die Beschreibung auf hohem Niveau (also ohne implementierungsspezifische Details) erfolgen und typischerweise so benannt sein, wie die Ziele aus Sicht der Akteure heißen: Mitglied anmelden, Geld abheben, Auto zurückgeben.

Jeder Anwendungsfall wird im selben Muster beschrieben. In den folgenden Absätzen ist zuerst eine allgemeine Beschreibung eines solchen Anwendungsfalls zu finden und dann ein Beispiel dazu.

Damit man auch versteht wer mit welchem Anwendungsfall agiert bietet es sich an hier eine Übersichtsgrafik zu erstellen:

![Übersicht Anwendungsfälle](img/anwendungsfalldiagramm.png){width=60%}

\newpage
### Anwendungsfallname
Anwendungsfälle haben einen eindeutigen Namen aus dem man auf den Inhalt des Anwendungsfalls schließen kann. Wenn Sie agil arbeiten dann stellt ein Anwendungsfall eine UserStory dar welche im Backlog liegt und im Laufe des Projekts (in einem Sprint) abgearbeitet wird.

#### Kurzbeschreibung
Hier erfolgt eine kurze Beschreibung, was im Anwendungsfall passiert. Kurz bedeutet, dass es zwei oder drei Zeilen sind, selten mehr.
      
#### Trigger
Der fachliche Grund bzw. die Gründe dafür, dass dieser Anwendungsfall ausgeführt 

#### Vorbedingung
Alle Bedingungen, die erfüllt sein müssen, damit dieser Anwendungsfall ausgeführt werden kann. Gibt es keine Vorbedingungen, so steht hier "keine".
      
#### Nachbedingung
Der Zustand, der nach einem erfolgreichen Durchlauf des Anwendungsfalls erwartet wird.

#### Akteure
Akteure sind beteiligte Personen oder Systeme außerhalb (!) des beschriebenen Systems. Z. B. Anwender, angemeldeter Anwender, Kunde, System, Abrechnungsprozess.

#### Standardablauf
Hier wird das typische Szenario dargestellt, das leicht zu verstehen oder der am häufigsten vorkommende Fall ist. An seinem Ende steht die Zielerreichung des Primärakteurs. Die Ablaufschritte werden nummeriert und meist in strukturierter Sprache beschrieben. Ablaufpläne können jedoch ebenfalls benutzt werden, wenn es angebracht erscheint. Mittels der UML können diese Ablaufschritte in Aktivitätsdiagrammen oder Anwendungsfall-orientierten Sequenzdiagrammen dargestellt werden.

#### Fehlersituationen
Dies sind Szenarien, die sich außerhalb des Standardablaufs auch bei der (versuchten) Zielerreichung des Anwendungsfalls ereignen können. Sie werden meistens als konditionale Verzweigungen der normalen Ablaufschritte dargestellt. An ihrem Ende steht ein Misserfolg, die Zielerreichung des Primärakteurs oder eine Rückkehr zum Standardablauf.

#### Systemzustand im Fehlerfall
Der Zustand, der nach einem erfolglosen Durchlauf des Anwendungsfalls erwartet wird.


\newpage
### Benutzer Anlegen

#### Kurzbeschreibung
Der Benutzer "Admin" kann auf Anfrage einen neuen Benutzer als "Lehrende" und bzw. oder "Studierende" anlegen

#### Trigger
Admin legt auf Anfrage eines Benutzers einen neuen Account an

#### Vorbedingung
Benutzer als "Admin" angemeldet
      
#### Nachbedingung
Es existiert ein Eintrag in der DB Benutzer Tabelle für den neu erstellten Benutzer. (Dieser kann sich anschließend in der Anwendung anmelden)

#### Akteure
* Admin

#### Fehlersituationen
Admin bricht die Aktion ab

#### Systemzustand im Fehlerfall
Benutzer wird nicht angelegt und wird verworfen

#### Standardablauf:

1. Admin drückt Button, um einen neuen Benutzer anzulegen
2. Es öffnet sich ein Formular, indem die nötigen Benutzer-Informationen eingegeben werden (Name, Adresse, Telephonnummer, E-Mail, Geburtsdatum, Passwort-Hash, Rolle). Der neue Benutzer muss mindestens einer der Rollen "Lehrende" und "Studierende" angehören

#### Alternativabläufe:

* Admin drückt den Button, um die Aktion abzubrechen 
