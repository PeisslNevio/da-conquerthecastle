# Teilaufgabe Schmiedpeter Rhys
\textauthor{Schmiedpeter}

## Blender {#sec32-theorie-blender}

### Einleitung in Blender

#### Möglichkeiten

Blender ist ein Programm mit vielfältigen Einsatzmöglichkeiten. Es eignet sich für die Modellierung, bietet eine Zeichenfunktion sowie einen Python-Editor. Zusätzlich können bestehenden Modellen Animationen hinzugefügt werden. Darüber hinaus lassen sich in Blender auch Videos rendern und schneiden [@blender_features] [@blender_manual].

#### Basics der Modellierung

Blender ist wie folgt aufgebaut: In der Mitte befindet sich das Koordinatensystem, in dem der Großteil der Arbeit stattfindet. Links liegen die wichtigsten Werkzeuge. Rechts befindet sich die Objekthierarchie mit Kamera, Licht und allen Objekten. Im unteren beziehungsweise rechten Bedienbereich befinden sich Funktionen wie Modifier, Material und Physik.

![Koordinatensystem [@blender]](img/schmiedpeter/Defaultscreen-blender.png){width=90%}

In der Modellierungsansicht gibt es drei Modi mit jeweils eigener Funktion:

- **Objektmodus:** Dieser Modus wird hauptsächlich für den Umgang mit mehreren Objekten und zum Einfügen neuer Objekte verwendet. Blender stellt standardmäßig Objekte wie Würfel, Quader, Zylinder oder Kugeln bereit. Diese sind zunächst auf Standardgröße gesetzt und können in Größe sowie Ursprung (`Set Origin`) angepasst werden. Außerdem werden in diesem Modus Funktionen wie Physik oder Modifier genutzt. Wichtige Werkzeuge sind Bewegen, Rotieren und Skalieren.
  
- **Editmodus:** Dieser Modus dient der Bearbeitung einzelner Objekte.

  > Der Modus funktioniert auch mit mehreren Objekten. Dies wird jedoch nicht empfohlen, weil dabei leicht ungewollte Fehler entstehen [@blender_manual].


  Die Auswahl funktioniert hier anders als im Objektmodus: Es werden keine ganzen Objekte, sondern Punkte, Kanten oder Flächen ausgewählt. Standardmäßig ist die Punktansicht aktiv. Nach demselben Prinzip funktionieren die Kanten- und Flächenansicht. *Tipp: Mit `Shift` können mehrere Elemente ausgewählt werden.*
  Wichtige Werkzeuge sind Loop Cuts und das Messer (zum Hinzufügen von Kanten), Bewegen, Einsetzen beziehungsweise Verkleinern von Flächen, Extrahieren und Füllen.

- **Skulpturmodus:** Dieser Modus nutzt Werkzeuge, die Polygone auf unterschiedliche Weise verformen. Dabei ist zu beachten, dass die Verformung nicht exakt maßbasiert erfolgt. Zusätzlich sollte das Objekt genügend Polygone besitzen, da das Ergebnis sonst häufig nicht den Erwartungen entspricht [@blender_manual].

Als Unterstützung in den jeweiligen Modi gibt es das Tool **Anmerkungen**. Damit können in der aktuellen Perspektive Markierungen eingezeichnet werden. Im Edit- und Objektmodus kann zusätzlich das Tool **Messen** verwendet werden. Dieses funktioniert ebenfalls perspektivbezogen und arbeitet wie die Anmerkungen in 2D.
  
\newpage

### Konkurrenz

Neben Blender hätten auch andere Modellierungsprogramme verwendet werden können, beispielsweise *Tinkercad, Autodesk Fusion oder OpenSCAD* [@blender_konkurrenz] [@blender_konkurrenz_tinkercad] [@blender_konkurrenz_autodesk] [@blender_konkurrenz_openscad].

- **Tinkercad:** Das Programm ist vor allem durch das einfache Entwerfen von Schaltungen bekannt und ähnlich niedrigschwellig ist auch die Modellierung. Es ist leicht verständlich und damit gut für Einsteiger geeignet. Für die Diplomarbeit war es jedoch zu eingeschränkt, da viele Formen nur mit vorgefertigten, kaum veränderbaren Grundobjekten erstellt werden können [@blender_konkurrenz_tinkercad].

- **Autodesk Fusion:** Dieses Programm ist stark auf Produktion, Werkzeuge und technische Konstruktion ausgerichtet, kann aber auch für die Modellierung eingesetzt werden. Die Handhabung gilt als gut und es wird von großen Unternehmen eingesetzt. Nachteilig sind die Lizenzkosten [@blender_konkurrenz_autodesk].

- **OpenSCAD:** OpenSCAD ist ein Open-Source-Programm für codebasierte Modellierung. Für dieses Projekt war es aufgrund der höheren Komplexität nicht die passende Wahl [@blender_konkurrenz_openscad].



### Nützliche Befehle

- **`Shift + A`**: Objekt hinzufügen.
- **`X`**: Löschen (mit Bestätigungsabfrage).
- **`TAB`**: Modus wechseln (Objektmodus/Editmodus).
- **`LEERZEICHEN`**: Zeitleiste abspielen/stoppen.

Für die folgenden Befehle gilt:

- Mit zusätzlichem Drücken von `X`/`Y`/`Z` wird auf die jeweilige Achse eingeschränkt.
- Mit `Shift` erfolgen feinere Bewegungen.

- **`G`**: Verschieben im Koordinatensystem.
- **`R`**: Drehen um den Ursprung (oranger Punkt).
- **`S`**: Skalieren um den Ursprung.

Für den Objektmodus:

- **`Strg + J`**: Objekte zusammenführen. Funktioniert mit zwei oder mehr Objekten; dabei bleibt ein aktives Primärobjekt erhalten (z. B. für den Ursprung).
- **`Rechtsklick` + Ursprung ändern**: Ursprung versetzen (z. B. nach Masse oder Volumen).
- **`Rechtsklick` + Weich schattieren**: Kanten optisch glätten, ohne Polygone hinzuzufügen.

Für den Editmodus:

- **`M`**: Punkte zusammenfügen. Funktioniert mit zwei oder mehr Punkten (bzw. Kanten/Flächen werden in Punkte umgewandelt); möglich auf erstem/letztem Punkt, in der Mitte oder beim Ursprung.
- **`Strg + R`**: Loop Cuts. Erstellt umlaufende Kanten; die Anzahl der Schnitte kann eingestellt werden.
- **`K`**: Messer. Fügt Schnitte in ein Objekt ein.
- **`E`**: Extrahieren. Erweitert Flächen bzw. Kanten.
- **`I`**: Einsetzen von Flächen. Erzeugt eine kleinere Fläche in einer größeren.
- **`F`**: Füllen von Flächen/Kanten. Bei zwei Punkten entsteht eine Kante, sonst eine Fläche; bei sehr vielen Punkten können ungünstige Flächen entstehen.
- **`Strg + T`**: Flächen in Dreiecke konvertieren. Sinnvoll für Export und Rendering.

\newpage

## Erweiterte Funktionen in Blender {#sec32-theorie-erweiterte-blender}

### Material

Material beschreibt das Aussehen eines Objekts bzw. einzelner Flächen. Dazu gehören unter anderem Farbe, Metalleffekt, Rauheit und weitere definierbare Eigenschaften. Standardmäßig ist ein Material neutral und hellgrau, damit Effekte und Farben die Modellierung nicht stören [@blender_manual].

![Material-Erklärung [@blender]](img/schmiedpeter/Material_blender.png){width=90%}

Objekte lassen sich im Editmodus einfärben. Einzelnen Flächen können Farben zugewiesen werden, indem zuerst die Flächen und danach das gewünschte Material ausgewählt werden. Damit die Farben sichtbar sind, muss das Shading auf Material-Vorschau oder Rendered gesetzt werden.



### Modifier

Modifier sind Erweiterungen mit eigenen Funktionen. Es gibt viele davon, in einem Projekt wird jedoch meist nur ein Teil tatsächlich genutzt. Manche Modifier erleichtern bestehende Arbeitsschritte, andere bieten zusätzliche Funktionen. Zu finden sind sie rechts unter dem Schraubenschlüssel-Symbol.

Modifier sind in Kategorien gegliedert; besonders relevant sind **Erzeugen** und **Physik**. Wichtig ist, dass Blender zunächst nur eine Vorschau zeigt. Erst nach dem Anwenden wird die Änderung dauerhaft in die Geometrie übernommen. Häufig verwendete Modifier sind Boolean, Mirror und Collision [@blender_manual].

#### Boolean

Mit dem Boolean-Modifier kann ein Objekt mit einem zweiten Objekt verrechnet werden. Je nach Modus sind **Schnittmenge, Vereinigung oder Differenz** möglich. Dafür werden ein primäres und ein sekundäres Objekt benötigt.

#### Mirror

Der Mirror-Modifier spiegelt ein Objekt entlang der gewählten Achse. Gespiegelt wird nicht um die geometrische Mitte, sondern um den Ursprung des Objekts.

#### Physik

Physik ist kein einzelner Modifier, sondern eine eigene Kategorie. Hier reagieren Objekte nach physikalischen Regeln der realen Welt. Möglich sind beispielsweise Simulationen mit Flüssigkeiten oder Stoffen. Viele Physik-Modifier benötigen ein zweites Objekt mit dem Modifier **Collision**, damit Kollisionen erkannt werden.

Ein typisches Beispiel ist der Cloth-Modifier. Er verhält sich wie ein Stofftuch: Startet man die Simulation mit `LEERZEICHEN`, fällt das Objekt nach unten. Befindet sich ein Collision-Objekt im Weg, bleibt der Stoff daran hängen. Da Flächen aus Polygonen bestehen, hängt die Qualität stark von der Geometrie und den Einstellungen (z. B. Gewicht, Steifigkeit) ab. Nach dem Anwenden wird die simulierte Form als fester Zustand übernommen.

\newpage

## Animationen {#sec32-theorie-animationen}
### Zweck und Nutzen von Animationen
Animationen sind notwendig, um statische Modelle in glaubwürdige, lesbare und emotionale Figuren zu verwandeln. In Spielen und Visualisierungen übernehmen sie mehrere Aufgaben: Sie machen Handlungen verständlich (z. B. Gehen, Angreifen), stärken die Identität einer Figur durch charakteristische Bewegungen und unterstützen die Spielmechanik durch klare Rückmeldungen (z. B. Treffer, Ausweichen). Ohne Animationen bleibt ein Modell ein reiner Blickfang, vermittelt jedoch keine Handlung und wirkt technisch wie dramaturgisch unvollständig.
[@blender_manual] 

### Grundlagen des Rigging mit Armature {#sec32-theorie-rigging}
Die Armature ist das Skelett einer Figur. Sie besteht aus Knochen (Bones), die hierarchisch verbunden sind und die spätere Bewegung definieren. Jeder Knochen besitzt einen Kopf und ein Ende; aus der Ausrichtung ergibt sich die lokale Achse, die für Rotationen entscheidend ist. Damit eine Armature sauber funktioniert, müssen die Skalierungen der Meshes angewendet sein, und die Bone-Orientierungen müssen konsistent angelegt werden.

**Parent-Knochen (Elternknochen)** bestimmen die Hierarchie. Bewegungen eines Elternknochens wirken auf alle darunterliegenden Kinderknochen. Dadurch lassen sich Ketten wie Wirbelsäule, Arm oder Bein logisch aufbauen. Ein Unterarm ist z. B. Kind des Oberarms, sodass eine Rotation des Oberarms die gesamte Kette mitführt.

![Armature-Struktur einer Figur](img/schmiedpeter/Armature.png){width=80%}

**Keep Offset** entsteht, wenn ein Knochen einem Elternknochen zugewiesen wird, seine aktuelle Position jedoch beibehält. Das bedeutet: Die Hierarchie wirkt, aber der Kindknochen verschiebt sich beim Parenten nicht an den Kopf des Elternknochens. Diese Variante ist sinnvoll, wenn der Abstand zwischen Knochen bewusst erhalten bleiben soll, z. B. bei Zubehör, Sekundärbewegungen oder technischen Rigs. Erstellt wird dies im Pose- oder Edit-Mode durch die Auswahl von Kind- und Elternknochen und anschließend `Strg + P` mit der Option Keep Offset. So bleibt der Abstand erhalten, die Vererbung der Bewegung ist jedoch aktiv.

![Keep Offset im Parenting-Vergleich](img/schmiedpeter/KeepOffset.png){width=80%}

**Inverse Kinematik (IK)** wird eingesetzt, wenn das Ende einer Knochenkette direkt gesteuert werden soll, z. B. Hände, Füße oder ein Knie beim Aufsetzen auf den Boden. Im Gegensatz zur Vorwärtskinematik (FK), bei der jeder Knochen einzeln rotiert wird, berechnet IK die Winkel der gesamten Kette automatisch, damit das Endglied ein Ziel erreicht. Technisch wird dazu ein Zielobjekt (IK-Target) definiert und ein IK-Constraint auf den Endknochen gesetzt; eine Kettenlänge bestimmt, wie viele Knochen beeinflusst werden. So lassen sich stabile Kontaktpunkte erzeugen, etwa wenn eine Hand eine Waffe hält oder ein Fuß sauber am Boden bleibt [@youtube_eCtSviaHZ6U].

### Anwendung an Figuren: Vorgehensweise
Für die Anwendung an einer Figur werden ein Mesh, eine Armature und eine klare Bindung zwischen beiden benötigt. Ziel ist es, dass die Knochenbewegung das Mesh nachvollziehbar verformt, ohne sichtbare Artefakte zu erzeugen. Eine Abbildung kann hier optional den Aufbau von Mesh, Armature und Gewichtung verdeutlichen.


Benötigte Schritte:

1. Mesh vorbereiten (Skalierung anwenden, Ursprung setzen).
2. Armature platzieren und Knochen entlang der geplanten Bewegung anordnen.
3. Parenting zwischen Mesh und Armature herstellen.
4. Gewichte (Weights) prüfen und bei Bedarf korrigieren.

Gerade bei organischen oder flexiblen Objekten ist die Verteilung der Gewichte entscheidend, da harte Übergänge die Bewegung unnatürlich wirken lassen.

![Armature im Mesh (On-Figure Ansicht)](img/schmiedpeter/OnFigure.png){width=80%}

### Gewichtung und Bindung des Meshes {#sec32-theorie-gewichtung}
Das Verbinden von Mesh und Armature erfolgt in Blender über das Parenting. Dabei gibt es mehrere Modi, die das Grundgerüst der Gewichtung erzeugen und den Ausgangspunkt für die spätere Feinabstimmung liefern:

**Automatic Weights**: Blender berechnet die Gewichte automatisch anhand der Nähe zu den Knochen. Dieser Modus ist effizient und liefert oft brauchbare Ergebnisse, ist jedoch bei komplexen Formen fehleranfällig. Typische Probleme sind ungewollte Verzerrungen, wenn Knochen zu nah an anderen Bereichen liegen. Deshalb ist eine anschließende manuelle Korrektur im Weight Painting fast immer notwendig. In der Praxis gilt: Automatic Weights sind der Startpunkt, nicht der Abschluss.

**With Empty Groups**: Erzeugt nur die notwendigen Vertex-Gruppen ohne Gewichte. Dieser Modus ist sinnvoll, wenn die Gewichtung bewusst manuell angelegt werden soll, etwa bei technischen oder sehr klar strukturierten Modellen.

**With Envelope Weights**: Nutzt die Bone-Envelopes (Einflussbereiche) anstelle einer Distanzberechnung. Der Vorteil liegt in der direkten Kontrolle über Einflussradien, allerdings ist die Methode bei feineren Strukturen weniger präzise und erfordert eine saubere Envelope-Konfiguration.

**Bone-Parenting (Bone)**: Das Mesh wird einem einzelnen Knochen untergeordnet. Diese Methode eignet sich für starre Objekte (z. B. Waffen, Schilder) und lässt keine organische Deformation zu.

![Gewichtungs-Vergleich bei Auswahl der Knochen](img/schmiedpeter/Gewichtungen.png){width=80%}

Nach dem Parenting werden die Gewichte mit den Gewichtungstools (Weight Paint) verfeinert. Sie steuern, wie stark ein Knochen einzelne Punkte des Meshes beeinflusst. Jeder Vertex erhält Gewichte in sogenannten Vertex-Gruppen, typischerweise mit Werten zwischen 0 und 1. Ein Wert von 1 bedeutet volle Beeinflussung durch den Knochen, ein Wert von 0 keine. In der Praxis werden die Gewichte über Pinselwerkzeuge gemalt, geglättet oder normalisiert, damit Übergänge weich bleiben und sich die Summe der Einflüsse pro Punkt sinnvoll verteilt. So entstehen organische Deformationen, ohne dass das Mesh unerwünscht einbricht oder sich verzieht [@blender_weight_paint_editing].

Wichtige Werkzeuge sind Add (Gewichte erhöhen), Subtract (Gewichte reduzieren), Blur oder Smooth (Übergänge glätten) sowie Normalize/Normalize All (Gewichte pro Vertex ausgleichen). Damit lassen sich harte Kanten vermeiden und Gelenkbereiche wie Ellbogen oder Knie sauber verformen.

\newpage

### Animation erstellen in Blender {#sec32-theorie-animation-erstellen}
Nach dem Rigging beginnt die eigentliche Animation im **Pose Mode** der Armature. Dabei werden nicht die Mesh-Punkte direkt bewegt, sondern die Knochen. Blender speichert diese Bewegungen als Keyframes und interpoliert die Zwischenbilder automatisch.
[@youtube_2nlMZx0vp6E] [@youtube_JQT9sT1YuAI] [@youtube_1khSuB6sER0]
Typische Vorgehensweise:

1. Armature auswählen und in den Pose Mode wechseln.
2. Zeitleiste auf den Startframe setzen (z. B. Frame 1).
3. Gewünschte Knochen in eine Startpose bringen.
4. Mit `I` Keyframes setzen (meist **Location**, **Rotation** oder **LocRot**).
5. Zur nächsten Zeitposition wechseln (z. B. Frame 12/24), neue Pose erstellen und erneut Keyframes setzen.
6. Dies für alle wichtigen Posen wiederholen (z. B. Kontaktpose, Passing Pose, Endpose).

Für saubere Ergebnisse werden die Kurven im **Graph Editor** oder die Keyframe-Reihenfolge im **Dope Sheet** nachbearbeitet. So lassen sich Bewegungen weicher, schneller oder härter gestalten [@youtube_08aXoov2qco].

Bei mehreren Animationen (z. B. Idle, Walk, Attack) sollte jede Bewegung als eigene **Action** im Action Editor gespeichert und klar benannt werden. Dadurch bleiben die Clips getrennt und können später in Unreal gezielt importiert werden.

Für Loops (z. B. Gehen) muss der letzte Frame zur Startpose passen, damit der Übergang ohne sichtbaren Sprung wieder von vorne beginnt.

### Einfügen in Unreal {#sec32-theorie-einfuegen-unreal}
Für den Export ist ein konsistentes Rig wichtig: gleiche Ausrichtung, klare Root-Struktur und einheitliche Benennung. In Unreal werden Armature und Animationen als FBX importiert. Entscheidend ist, dass die Animationen im selben Skeleton bleiben, damit sie austauschbar und wiederverwendbar sind. So kann z. B. eine Geh-Animation an mehreren Figuren genutzt werden, solange das Skelett kompatibel bleibt.

Kurzablauf für den Import:

1. In Blender als `FBX` exportieren (Mesh + Armature + gewünschte Animationen).
2. In Unreal im Content Browser `Import` wählen und die FBX-Datei laden.
3. Beim ersten Import ein neues Skeleton erzeugen, bei weiteren Animationen **dasselbe** Skeleton auswählen.
4. `Import Animations` aktivieren, damit die Actions als Animation Sequences übernommen werden.
5. Importierte Clips im Animation Preview testen (Loop, Geschwindigkeit, Root-Bewegung).

Wenn ein Clip nicht korrekt aussieht, liegt dies meist an Bone-Namen, Skalierung oder nicht angewendeten Transformationen in Blender.

## Game Sound {#sec32-theorie-gamesound}

Game Sound ist weit mehr als akustische Dekoration. Im Computerspiel übernimmt er eine doppelte Funktion: Einerseits erhöht er die Immersion, indem er die künstliche Spielwelt mit glaubwürdigen Klangräumen füllt, andererseits liefert er dem Spieler unmittelbares Feedback auf Handlungen, Ereignisse und Zustandswechsel. Fehlen Hintergrundgeräusche, wirkt eine Szene schnell künstlich und leer; sind sie stimmig gestaltet, werden sie oft kaum bewusst wahrgenommen, stabilisieren jedoch das Erleben der Spielwelt nachhaltig.

Im Unterschied zu linearen Medien entsteht Sound im Spielkontext unter interaktiven Bedingungen. Atmo, Musik, Sprache und Geräusche werden nicht in einer fixen Reihenfolge abgespielt, sondern können sich abhängig von Spieleraktionen zeitlich unvorhersehbar überlagern. Genau daraus ergeben sich zentrale gestalterische Herausforderungen: Sprachverständlichkeit muss erhalten bleiben, klangliche Konflikte zwischen Ebenen sollen vermieden werden, und trotzdem muss ein konsistenter Gesamteindruck entstehen. Eine strukturierte Klanghierarchie und ein bewusstes Lautstärke- und Mischungsverhältnis sind daher Grundvoraussetzungen für professionellen Gamesound.

### Musikpsychologische Grundlagen {#sec32-theorie-musikpsych}
#### Wahrnehmung von Tönen
Die Wahrnehmung von Tönen wird in der musikpsychologischen Lehre von Ernst Kurth als Erleben von „Strebewirkungen“ beschrieben: Töne und Intervalle wirken nicht statisch, sondern erzeugen den Eindruck von gerichteter Bewegung, Spannung und möglicher Auflösung. Die Strebetendenz-Theorie (Willimek) erweitert diesen Ansatz, indem sie diese Wirkung als psychologische Identifikation des Hörers mit Willensregungen deutet. Vereinfacht bedeutet das: Der Hörer erlebt nicht nur eine Klangbewegung, sondern einen inneren Impuls gegen oder für eine Veränderung [@willimek_musik_und_emotionen_2011].

> „Wir erleben einen Ton nicht als Frequenz, sondern als undefinierbares Ding, das wir jedoch nicht als sinnvoll in unsere materielle Welt eingegliedert erfahren können.“ (Musik und Emotionen, S. 3)

Diese Sichtweise verdeutlicht, dass Töne nicht nur als messbare physikalische Signale verarbeitet werden, sondern als psychisch bedeutungsvolle Klangereignisse [@willimek_musik_und_emotionen_2011].

Für Leitton- und Vorhaltswirkungen wird dieses Prinzip konkret über Spannung erklärt. Dissonante Reibungen (z. B. Sekundreibungen im Obertonbereich) werden teilweise unbewusst wahrgenommen und erzeugen ein Spannungsfeld, das eine Auflösung erwartet. Daraus entsteht der typische Eindruck von Erwartung und Zielgerichtetheit in musikalischen Verläufen. Für den Gamesound ist dieser Mechanismus zentral, weil er genutzt werden kann, um Aufmerksamkeit zu lenken, Unsicherheit zu steigern und Auflösungsmomente dramaturgisch wirksam zu gestalten.

#### Basisemotionen
Im Kontext von Musik und Emotionen werden Basisemotionen nicht isoliert betrachtet, sondern als Ergebnis mehrerer Parameter, vor allem Harmonik, Tempo und Lautstärke. In den dargestellten Testansätzen wurden Musikbeispiele bewusst auf wenige Parameter reduziert, um den emotionalen Kern sichtbar zu machen. Dabei zeigt sich: Das Zusammenspiel aus harmonischer Struktur sowie zeitlicher und klanglicher Gestaltung bestimmt maßgeblich die wahrgenommene Emotion.

Eine besondere Rolle spielt das Tempo. Schnellere Verläufe erhöhen typischerweise Aktivierung und werden häufiger mit Erregung, Anspannung oder Durchsetzungskraft verbunden, während langsamere Verläufe eher Ruhe, Trauer oder Gelöstheit stützen. Zusätzlich zeigen physiologische Befunde, dass aktivierende Musik mit erhöhter Herzfrequenz und Muskelspannung korreliert, beruhigende Musik hingegen mit sinkender Herzfrequenz. Damit wird die emotionale Wirkung nicht nur subjektiv beschrieben, sondern auch körperlich nachvollziehbar [@willimek_musik_und_emotionen_2011] [@neurophysiological_emotion_analysis_music_2014].

Typische emotionale Zuordnungen aus den dargestellten Harmoniezusammenhängen sind:

- **Dur-Tonika**: nüchternes Einverstanden-Sein mit dem Gegenwärtigen.
- **Moll-Tonika**: Trauer (bei leiser/langsamer Ausprägung) oder Zorn (bei lauter/schneller Ausprägung).
- **Äolisches Moll**: Mut, Abenteuer, Spannung, Gefahr.
- **Subdominante in Dur**: Freude, Überschwänglichkeit, Feierlichkeit.
- **Verminderter Septakkord / kleine Sexte**: Schrecken, Verzweiflung, Bedrohung, Angst.
- **Übermäßiger Dreiklang**: Staunen, Überraschung, Verwandlung.

Diese Zuordnungen sind für Gamesound praktisch nutzbar, weil sie eine gezielte Kopplung von Spielsituation und musikalischem Ausdruck erlauben (z. B. Gefahrensignal, Triumphmoment, Trauerphase).

![Notenabbildung zu Harmoniewirkungen](img/schmiedpeter/Noten_Abb.png){width=70%}

#### Mechanismen der Musikemotion
Ein etablierter Erklärungsrahmen für musikalisch ausgelöste Emotionen ist das BRECVEM-Modell nach Juslin & Västfjäll. Es beschreibt sieben unterschiedliche Auslösemechanismen, die parallel oder kombiniert wirken können [@neurophysiological_emotion_analysis_music_2014]:

- **B – Brain Stem Reflex**: Plötzliche, laute, dissonante oder sehr schnelle Signale lösen unmittelbare Alarm- bzw. Aktivierungsreaktionen aus.
- **R – Rhythmic Entrainment**: Externe Rhythmen synchronisieren innere Rhythmen (z. B. Herzrate), wodurch Aktivierung und Erregung mitgesteuert werden.
- **E – Evaluative Conditioning**: Musik wird emotional wirksam, weil sie wiederholt mit positiven oder negativen Ereignissen gekoppelt wurde.
- **C – Emotional Contagion**: Hörer übernehmen den wahrgenommenen emotionalen Ausdruck der Musik durch innere Nachbildung.
- **V – Visual Imagery**: Musik erzeugt innere Bilder, die wiederum Emotionen auslösen oder verstärken.
- **E – Episodic Memory**: Musik aktiviert autobiografische Erinnerungen und damit verbundene Gefühle.
- **M – Musical Expectancy**: Erwartungen an den Fortgang der Musik werden erfüllt, verzögert oder verletzt; daraus entstehen Spannung, Überraschung und Auflösung.

Gerade für interaktive Medien ist dieses Modell hilfreich, weil es zeigt, dass Musikemotionen nicht nur über Harmonik entstehen, sondern auch über Konditionierung, Rhythmuskopplung, Erwartungssteuerung und Erinnerungseffekte vermittelt werden.

### Interaktive Musik in Videospielen {#sec-interaktive-musik}
Interaktive Musik ist im Gamesound kein statischer Hintergrund, sondern ein steuerbares System [@collins_game_sound] [@hofmann_szczypula_game_sound_2006].

Ihre zentrale Aufgabe besteht darin, das Spielgeschehen emotional zu unterstützen, ohne den Spielfluss zu stören.

Im Unterschied zur Filmmusik ist der genaue Zeitpunkt von Szenenwechseln oder Gefahrensituationen im Spiel oft nicht vorhersehbar. Deshalb muss Musik flexibel auf Spielerhandlungen reagieren und trotzdem musikalisch zusammenhängend bleiben.

#### Adaptive vs. dynamische Musik

Im praktischen Einsatz lassen sich zwei komplementäre Verfahren unterscheiden, die oft kombiniert werden:

**Adaptive Musik** funktioniert zustandsorientiert. Sie wechselt zwischen vordefinierten Musikzuständen (States), die jeweils an eine konkrete Spielsituation gebunden sind. Mit **Musikzuständen** sind klar definierte Spielphasen gemeint, beispielsweise:

- **Erkundung** (ruhig, wenig rhythmische Dichte),
- **Gefahr im Anmarsch** (wachsender Puls/Spannung),
- **Kampf** (hohe Intensität, dichteres Arrangement),
- **Nach dem Kampf** (Reduktion und Entspannung).

Der Wechsel zwischen diesen States wird durch konkrete Spielparameter ausgelöst – etwa Gegnernähe, Alarmstatus, Lebenspunkte, Ortswechsel oder Missionsfortschritt. Die Musik wechselt, wenn der State eintritt, und bleibt in diesem Zustand, bis sich eine neue Spielbedingung ergibt.

**Dynamische Musik** hingegen arbeitet parametrisch und kontinuierlich. Während ein Musikstück läuft, werden einzelne Parameter in Echtzeit angepasst – nicht der State selbst, sondern die Eigenschaften der bereits laufenden Musik. Typische dynamische Parameter sind:

- **Lautstärke:** Erhöhung bei Gegnerannaherung, Reduktion bei Sicherheit,
- **Instrumentierung:** Hinzufügen von aggressiveren Instrumenten oder Entfernung von beruhigenden Pads mit wachsender Gefahr,
- **Rhythmische Dichte:** Das Tempo der Schlagzeug- oder Bassmuster wird schneller/komplexer, je intensiver die Situation wird,
- **Filterung:** Hochpass- oder Tiefpassfilter verändern die Klarheit oder Dunkelheit des Klangs je nach Atmosphäre.

Ein konkretes Beispiel: Ein Boss-Kampf könnte mit einem Musikstück im "Kampf"-State beginnen. Während der Spieler den Boss bekämpft, werden Lautstärke und Rhythmusdichte dynamisch an die verbliebenen Lebenspunkte des Gegners angekoppelt. Sinken diese kritisch ab, könnte ein zusätzlicher Streicher-Swell hinzugefügt werden, ohne den State zu wechseln. Nach dem Kampf erfolgt dann der Umschlag auf den State "Nach dem Kampf".

**Zusammenhang:** 

Beide Ansätze verfolgen dasselbe Ziel: Die Musik soll den aktuellen Spielzustand hörbar machen. Adaptive Musik bietet große emotionale Sprünge (z. B. von Erkundung zu Kampf), während dynamische Musik feinere Abstufungen ermöglicht. Diese Reaktionsfähigkeit ist entscheidend, weil in interaktiven Medien mehrere Soundebenen (Atmosphäre, Geräusche, Sprache, Musik) gleichzeitig aktiv sein können. Musik muss daher nicht nur emotional passen, sondern sich auch in das Gesamtmixing einordnen, damit die Sprachverständlichkeit nicht leidet.

#### Looping-Techniken
Looping ist eine Grundtechnik interaktiver Musik, da Spielsituationen unterschiedlich lange dauern. Musik wird deshalb meist als nahtloser Kreis aufgebaut, damit keine hörbaren Brüche entstehen, wenn ein Abschnitt länger aktiv bleibt.

Für professionelle Übergänge zwischen Zuständen werden laut den beschriebenen Produktionsansätzen vor allem zwei Verfahren genutzt:

- **Überblendung (Crossfade)** zwischen zwei Musikzuständen.
- **Takt- oder phasenbezogener Wechsel**, bei dem der Übergang an musikalisch sinnvollen Punkten erfolgt.

In der Praxis ist die Überblendung robuster, weil sie auch bei unvorhersehbaren Spieleraktionen funktioniert. Taktgenaue Wechsel klingen musikalisch sauberer, benötigen jedoch ein enger abgestimmtes Musiksystem [@collins_game_sound].

#### Layer-Systeme
Layer-Systeme teilen einen Musikzustand in mehrere Ebenen, die je nach Spielsituation zu- oder abgeschaltet werden. Typische Layer sind z. B. Rhythmus, Harmonie, Flächen oder Percussion-Akzente. Dadurch kann die Musik stufenlos verdichtet werden, ohne dass das Grundthema wechselt.

Der Vorteil liegt in der hohen Kontrolle über Intensität und Dramaturgie:

- Bei ruhigen Phasen laufen nur Basis-Layer.
- Bei steigender Gefahr werden zusätzliche Layer aktiviert.
- Nach einer Entspannung werden Layer wieder reduziert.

Dieses Verfahren passt besonders gut zu den Anforderungen interaktiver Klanggestaltung, weil es musikalische Kontinuität mit klarer Spielrückmeldung kombiniert und Überlagerungen mit Sprache und Atmo besser steuerbar macht.

#### Produktionswerkzeuge im Kontext interaktiver Musik
Die zuvor beschriebenen Konzepte (States, Layer, Looping, Übergänge) werden in der Praxis meist in einer **Digital Audio Workstation (DAW)** vorbereitet. Eine DAW dient dabei als Produktionsumgebung, in der musikalische Bausteine komponiert, arrangiert, gemischt und für den späteren Einsatz in der Engine exportiert werden.

Eine zentrale Rolle spielt dabei **MIDI**. MIDI enthält keine Audiodaten, sondern Steuerinformationen (z. B. Tonhöhe, Länge, Velocity, Timing). Dadurch können musikalische Ideen schnell variiert, instrumentiert und an unterschiedliche Intensitätsstufen angepasst werden. Gerade für adaptive und dynamische Spielmusik ist diese Flexibilität wichtig, weil Material häufig in mehreren Versionen (z. B. ruhig, mittel, intensiv) benötigt wird [@collins_game_sound],[@hofmann_szczypula_game_sound_2006].

\newpage

## Praktisch

### Design

Die grundlegende Inspiration stammt von den Rittern des Mittelalters. Vor allem in der Rüstungskonstruktion zeigt sich dieser Bezug deutlich. Verwendet wurde eine Kombination aus Kettenrüstung sowie Helm und Brustpanzer mit Arm- und Beinschienen.

Die Kettenrüstung ist jedoch nicht gut geeignet für den Modellierungsstil **Low-Poly**.

#### Low-Poly-Stil

Low-Poly ist ein einfach gehaltener Stil mit relativ wenigen Polygonen (Punkten).  
Der große Vorteil dieses Stils liegt vor allem in der Performance [@low_poly] [@why_low_poly].

Grundsätzlich gilt:
> Je weniger Punkte ein Modell besitzt, desto weniger muss der PC beim Rendern berechnen.

Um zu überprüfen, wie viele Punkte ein Modell besitzt, kann es exportiert und anschließend als **FBX-Datei** betrachtet werden. Auf **3dviewer.net** erhält man dazu eine gute Übersicht.

#### Helmgestaltung {#helmgestaltung}

Eine weitere unübliche Gestaltung ist der Helm. Untypisch sind dabei vor allem die Hörner sowie generell die auffällige Farbgestaltung. Hörner an Helmen gab es im Mittelalter nur sehr selten. Wahrscheinlich wurden sie damals kaum verwendet, da sie im Kampf eher hinderlich waren.

#### Farbwahl

Die Farben wurden bewusst gewählt, da sie eine klare Funktion erfüllen.  
Sie unterstützen die Darstellung des Bosses als Oberhaupt des Gegners und tragen zusätzlich eine symbolische Bedeutung.

Die Farbe **Lila** wird beispielsweise häufig mit Macht, Reichtum und Autorität assoziiert. Historisch gesehen war Lila zudem eine Farbe, die sehr schwer herzustellen war und daher auch im Mittelalter als Zeichen von Wohlstand galt.

#### Zeitliche Einordnung der Rüstung

Die Rüstung selbst erinnert eher an das **Hoch- bzw. Spätmittelalter** beziehungsweise an die **Renaissance**, da in diesen Epochen Rüstungen immer kunstvoller gefertigt wurden.

- **Hoch- und Spätmittelalter (ca. 1380–1500)**  
  Diese Epoche bietet sehr guten Rundumschutz am gesamten Körper und eignet sich daher gut für ein Low-Poly-Design.

- **Renaissance**  
  In dieser Zeit wurden Rüstungen sehr detailreich gestaltet, was für Low-Poly-Modelle weniger geeignet ist. Typisch dafür sind stark verzierte Rüstungen oder Elemente wie Kappenhelme und aufwendige Verzierungen.

### Umsetzung mit Blender
#### Modellierung
**Entwickelte Techniken**

Im Verlauf eines längeren Projekts werden immer wieder neue Funktionen entdeckt. Teilweise entstehen dabei auch eigene Arbeitsweisen. In Blender wurden unter anderem die folgenden Techniken genutzt:

- **Alternative zu Insert:** Eine Fläche wird ohne zusätzliche Höhe extrahiert und anschließend mit `S` skaliert. Dabei ist darauf zu achten, dass sich keine Flächen überschneiden.
- **Objekte auf Kreisbahn verschieben:** Diese Technik nutzt einen frei gesetzten Ursprung. Für Objekte auf einer kugelförmigen Oberfläche wird derselbe Ursprung wie bei der Kugel gesetzt. Mit `R` kann das Objekt dann im gleichen Abstand bzw. mit gleicher Neigung entlang der Kugel bewegt werden (siehe Abbildung).

![Objekte auf einer Kugel [@blender]](img/schmiedpeter/kugel_bewegen.png){width=50%}

- **Skizzenbasierter Aufbau:** Formen wurden zunächst mit Anmerkungen vorgezeichnet und danach in der 2D-Ansicht ausgearbeitet. Diese Methode ist einfacher als klassisches UV-Mapping.

**Vorgehensweise**

Das Design war bereits grob festgelegt, daher musste eine sinnvolle Umsetzungsstrategie definiert werden. Der Start erfolgte beim Kopf, anschließend wurde nach unten weitergearbeitet. Die Gliedmaßen wurden bewusst später ausgearbeitet. Die Reihenfolge lautete: Helm und Kopf, danach Körper, anschließend Hals als Verbindung sowie danach Beine und Arme; zum Schluss folgten Füße und Hände. [@mio3_uv_addon] [@edgeflow_addon] [@blender_python_api_247_module]

Die Modellierung des Bosses erfolgte nach dem Prinzip, von oben nach unten zu arbeiten, wobei die Gliedmaßen bewusst erst am Ende ausgearbeitet wurden. Diese Vorgehensweise erleichterte es, zunächst die grundlegenden Proportionen und die visuelle Wirkung der Figur festzulegen, bevor Details ergänzt wurden. Der Fokus lag dabei auf einer klaren Silhouette und einer gut erkennbaren Formensprache, die bereits aus der Distanz die Rolle des Bossgegners vermittelt.

Die folgende Abbildung zeigt den fertig modellierten Boss als Ergebnis dieses Arbeitsschritts.

![Fertig modellierter Boss](img/schmiedpeter/Boss_fertig.png){width=70%}

**Helm**

Die praktische Ausarbeitung des Helms baut auf den zuvor beschriebenen Gestaltungsentscheidungen auf (vgl. [Helmgestaltung](#helmgestaltung)). Die Kopfform wurde bewusst höher als rund gestaltet und orientiert sich eher an einer quaderartigen Grundform. Dadurch wirkt der Kopf massiver und dominanter, was die bedrohliche Erscheinung des Bosses zusätzlich verstärkt. Die Gesichtsform weist einen klaren, basalen Schnitt auf, der gezielt hervorgehoben wurde. Das Visier wurde leuchtend gestaltet, um einen mysteriösen und leicht übernatürlichen Eindruck zu erzeugen.

Ein weiteres markantes Merkmal des Helms sind die Hörner. Diese verlaufen mit ihrer Masse nach hinten, wurden jedoch relativ flach gehalten, um die Gesamtform nicht zu überladen. Während der Modellierung zeigte sich, dass die Spitzen der Hörner zunächst an einer falschen Position lagen. Aus diesem Grund wurden sie im weiteren Verlauf neu ausgerichtet, sodass sie sich harmonisch in die Gesamtform des Helms einfügen und die Silhouette nicht negativ beeinflussen.

**Körper**

Beim Körper wurde eine spezielle Modellierungstechnik eingesetzt, bei der quer verlaufende Akzente genutzt wurden, um die körperlichen Strukturen gezielt hervorzuheben. Der Fokus lag dabei insbesondere auf der Brust- und Bauchmuskulatur sowie auf den Schultern, da diese Bereiche maßgeblich zur kraftvollen und einschüchternden Wirkung des Bosses beitragen. Zusätzlich wurden auch sekundäre Elemente wie der Gürtel in das Modell integriert, um den Gesamteindruck stimmig abzurunden.

Im nächsten Schritt wurde eine Cloth-Simulation angewendet, um der Rüstung ein realistischeres Verhalten zu verleihen (vgl. [Erweiterte Funktionen in Blender](#sec32-theorie-erweiterte-blender)). Nach Abschluss dieses Arbeitsschritts wurden nicht mehr benötigte Körperteile unter der Rüstung entfernt. Diese Entscheidung wurde aus Performancegründen getroffen, da verdeckte Geometrie im finalen Spielmodell keinen visuellen Mehrwert bietet, jedoch unnötig Rechenleistung beansprucht.

**Hals**
Der Hals wurde bewusst als verbindendes Element zwischen Helm und Körper modelliert. Ziel war keine stark ausgeprägte Eigenform, sondern ein stabiler Übergang, der die Proportionen zusammenführt und die Silhouette technisch wie optisch schlüssig hält.

**Beine**
Die Beine entstanden aus einem längeren Zylinder mit mehreren Vertices, um genügend Geometrie für spätere Verformungen zu erhalten. Im Kniebereich wurde die Form leicht verjüngt und anschließend im Sculpt-Modus mit zusätzlicher Tiefe und Detail versehen.

Besonders beachtet wurde, dass das Knie vorne etwas stärker ausgeprägt ist und auf der Rückseite eine kleine Einbuchtung besitzt. Diese Form unterstützt eine glaubwürdigere Beweglichkeit, da die Gelenkzone beim Beugen mehr Platz erhält.

**Arme**

Die Arme wurden nach demselben Grundprinzip wie die Beine aufgebaut: zunächst ein länglicher Grundkörper mit ausreichender Segmentierung, danach gezielte Formanpassungen für Gelenkbereiche und Volumenverteilung. Dadurch blieb die Modellierung konsistent und ließ sich gut in die Gesamtfigur integrieren.

**Hände**
Die Hände wurden separat modelliert, um Form und Topologie präziser steuern zu können. Entscheidend war dabei die Verteilung der Vertices in den Fingergelenken. In diesen Bereichen wurde zusätzliche Geometrie vorgesehen, damit Fingerbewegungen bei späterer Animation sauber deformieren und keine harten Knicke entstehen.

Zusätzlich wurden Proportionen und Übergänge zur Armgeometrie mehrfach nachgearbeitet, damit die Hände sowohl im statischen Modell als auch in Bewegung stimmig wirken.

**Probleme und Lösungen**
Im Körperbereich traten Form- und Topologieprobleme auf: Die Rüstung war an den Seiten zu dünn und am Rücken stellenweise zu flach, einzelne Eckpunkte waren durch überlagernde Flächen schwer erreichbar, und an mehreren Stellen liefen Vertices durch den Körper. Zusätzlich waren Übergänge fehlerhaft verbunden, sodass unter anderem zwischen Schulter und Rumpf sowie im Handbereich Lücken entstanden. Diese Bereiche wurden durch gezielte Skalierung korrigiert; bei fehlerhafter Topologie wurden Arbeitsschritte zurückgesetzt und in korrekter Reihenfolge neu aufgebaut.

Diese Übergänge wurden manuell korrigiert: Fehlerhafte Vertices wurden gelöscht, neu gesetzt und die betroffenen Bereiche anschließend sauber zusammengeführt. Dadurch konnten offene Kanten und sichtbare Spalte im Mesh weitgehend geschlossen werden.

Ein weiteres Problem waren nicht-manifold Geometrien. Darunter versteht man Geometrieelemente, die keine saubere, geschlossene Oberfläche bilden (z. B. lose, doppelte oder topologisch fehlerhafte Kanten und Vertices). Zur Bereinigung wurde zuerst `Mesh > Clean Up > Merge by Distance` verwendet, um überlappende Punkte zu verschmelzen. Danach wurden über `Select > Select All by Trait > Non Manifold` problematische Stellen markiert und anschließend händisch nachbearbeitet.

Durch diese Kombination aus automatischer Bereinigung und manueller Korrektur wurde das Mesh deutlich stabiler und besser für weitere Schritte wie Rigging, Animation und Export vorbereitet (vgl. [Grundlagen des Rigging mit Armature](#sec32-theorie-rigging), [Animation erstellen in Blender](#sec32-theorie-animation-erstellen), [Einfügen in Unreal](#sec32-theorie-einfuegen-unreal)).

### Animationen
#### Vorgehensweise beim Rigging
Die Animationen wurden auf Basis des im Theorieteil beschriebenen Rigging-Ansatzes erstellt (vgl. [Grundlagen des Rigging mit Armature](#sec32-theorie-rigging), [Gewichtung und Bindung des Meshes](#sec32-theorie-gewichtung), [Animation erstellen in Blender](#sec32-theorie-animation-erstellen)). Zuerst wurde eine eigene Armature aufgebaut, inklusive Inverser Kinematik (IK) und Offset-Setups, um kontrollierbare Gelenkbewegungen und saubere Hierarchien zu erhalten.

Anschließend wurden zwei Varianten getestet: die manuell aufgebaute Armature und ein automatisiert erzeugtes Rig. Beide Varianten wurden mit automatischer Gewichtung an den Boss gebunden und praktisch im Animationsprozess verglichen.

Die folgende Abbildung zeigt das praktische Rigging-Setup; **gelb steht für die Inverse Kinematik (IK)**.

![Armature mit IK (Gelb = Inverse Kinematik)](img/schmiedpeter/Armature_mit_IK.png){width=60%}


Die folgende Abbildung zeigt das in Blender erzeugte Rigify-Kontroll-Rig. Sichtbar sind die typischen Controller-Formen; die Controls sind überwiegend blau dargestellt, während gelbe Elemente die IK-relevanten Bereiche markieren.

#### Einsatz von Rigify
Für den Vergleich wurde das Blender-Addon **Rigify** verwendet. Der Vorteil von Rigify liegt in der schnellen Erstellung eines funktionsfähigen Kontroll-Rigs, das für die Animation meist angenehmer und effizienter zu bedienen ist als ein vollständig manuell aufgebautes Setup.


![Armature Rigify (Kontroll-Rig)](img/schmiedpeter/Armature_Rigify.png){width=80%}

In der praktischen Arbeit zeigte sich, dass sich das Rigify-Rig für die meisten Bewegungen besser steuern ließ. Gleichzeitig wurden nicht alle automatisch erzeugten Knochen verwendet, insbesondere im Gesichtsbereich. Diese Teile waren für den benötigten Animationsumfang nicht erforderlich und wurden deshalb im Workflow bewusst ausgeklammert.

Zusätzlich ist relevant, dass Rigify standardisierte Grundriggerüste bereitstellt, unter anderem für humanoide Figuren und für vierbeinige Tiere. Dadurch eignet sich das Addon gut als Ausgangspunkt für unterschiedliche Charaktertypen.

#### Recherche und Nutzung von Mixamo
Bei der Recherche zu geeigneten Animationsquellen wurde die Plattform **Mixamo** von Adobe einbezogen. Mixamo bietet vorkonfigurierte Bewegungsabläufe, die direkt auf Charaktere angewendet und anschließend exportiert werden können. Dadurch lassen sich grundlegende Animationen schnell testen und in einen eigenen Workflow integrieren.

Ein Teil der Animationen wurde aus Mixamo übernommen. Mehrere dieser Clips mussten jedoch nachbearbeitet werden, damit Timing, Haltung und Übergänge zur Figur und zum Spielkontext passen. Zusätzlich wurden einzelne Bewegungen vollständig selbst erstellt, da die verfügbaren Vorlagen die gewünschte Wirkung nicht ausreichend abdeckten.

#### Schwierigkeiten und Probleme
Während der Animationsphase traten vor allem Unterschiede zwischen importierten und eigenen Bewegungsabläufen auf. Die größten Herausforderungen lagen in der konsistenten Übergangsqualität zwischen Clips sowie in der Anpassung einzelner Posen an die Proportionen des Boss-Charakters.

Gelöst wurde dies durch schrittweise Korrekturen im Pose- und Graph-Workflow, gezielte Anpassung der Keyframes und eine vereinheitlichte Struktur der verwendeten Animationen. Dadurch konnte ein stimmiger Bewegungsablauf mit wiederverwendbaren Clips aufgebaut werden.

### Musik

#### Produktionsumgebung
Für die Musikproduktion wurde **Reaper** als zentrale DAW (Digital Audio Workstation) eingesetzt. Ergänzend kamen **MIDI-Inhalte aus Splice Instruments** zum Einsatz. Diese Kombination ermöglichte einen schnellen Einstieg in die Komposition, flexible Anpassungen von Arrangement und Dynamik sowie eine effiziente Ausarbeitung mehrerer Musikzustände [@collins_game_sound] [@hofmann_szczypula_game_sound_2006],[@reaper_official] [@splice_official].

Für die praktische Musikgestaltung und Musiksteuerung in Unreal wurden ergänzend Tutorials zur dynamischen Musikumschaltung und zur levelübergreifenden Musikwiedergabe verwendet [@youtube_8wbtWj_MQ9w] [@youtube_izH206dOhNQ].

Ein zentraler praktischer Befund war der hohe Zeitaufwand: Bis Idee, Stimmung, Dramaturgie und technische Einsetzbarkeit zusammenpassen, sind mehrere Iterationen aus Komponieren, Testen und Überarbeiten nötig.

Ein weiterer wichtiger Praxispunkt war die Bearbeitung der MIDI-Velocity: Die Anschlagsstärken wurden bewusst grob variiert, da gleichförmige Velocity-Werte schnell zu einem maschinellen Klang führen. Durch diese Variation wirkt die Musik lebendiger, und die gewünschte emotionale Wirkung kommt deutlich stärker zur Geltung.

#### Musikalisches Gesamtkonzept
Die Musik des Projekts wurde bewusst düster konzipiert, um die bedrohliche Atmosphäre des Bosskampfs zu tragen und emotional zu verdichten. Der Ansatz orientiert sich an den im Theorieteil dargestellten Zusammenhängen zwischen Harmonik, Tempo, Dynamik und emotionaler Wirkung (vgl. [Musikpsychologische Grundlagen](#sec32-theorie-musikpsych)) [@schulz_entwicklung_musik_videospielen_2022] [@collins_game_sound] [@youtube_music_controls_you].

Durch dunkle Klangfarben, spannungsorientierte Verläufe und klar gestufte Intensitäten wird die Wahrnehmung von Gefahr, Unsicherheit und Eskalation gezielt verstärkt. Die detaillierte psychologische Herleitung der einzelnen Stücke wird in einem späteren Arbeitsschritt ergänzt [@youtube_write_music_for_games] [@youtube_music_transcends_game].

#### Vorgehensweise und Einteilung
Zu Beginn wurde strukturiert festgelegt, welche Musik- und Soundelemente im Spiel benötigt werden. Die konzeptionelle Orientierung erfolgte dabei über unterschiedliche Referenzquellen: Beiträge und Analysen von Creator:innen auf YouTube, musikalische Eindrücke aus Spotify sowie Vergleichswerte aus anderen Spielen und Filmen. Diese Referenzen dienten nicht als direkte Übernahme, sondern als Grundlage für Stimmung, Klangfarbe und dramaturgische Ausrichtung der eigenen Kompositionen.

Zusätzlich floss das im Theorieteil erarbeitete Wissen gezielt in die praktische Umsetzung ein, insbesondere zu Zustandswechseln, Layering und musikalischer Reaktionslogik (vgl. [Musikpsychologische Grundlagen](#sec32-theorie-musikpsych) und [Interaktive Musik in Videospielen](#sec-interaktive-musik)).

Daraus ergab sich folgende Einteilung:

- **Titelmusik**

Die Titelmusik führt in die düstere Spielwelt ein und bereitet den Spieler emotional auf den finalen Bosskampf vor. Als tonales Fundament wurde D äolisch gewählt, da Moll-Tonalität und insbesondere die kleine Sexte (Bb) eine spannungsgeladene, bedrohliche Wirkung unterstützen. Eine Dur-Auflösung wird bewusst vermieden, um keine vorzeitige emotionale Entlastung zu erzeugen.
Das langsame Tempo (60 BPM) sowie der Verzicht auf Percussion reduzieren die physiologische Aktivierung und lenken den Fokus auf Atmosphäre und Raumwirkung. Die reduzierte Instrumentation aus Cello, tiefen Streichern und Chor unterstützt die mittelalterliche Ästhetik und erzeugt ein Gefühl von Schwere und Monumentalität.
Das Leitmotiv (D–F–Bb–A) wird im späteren Bosskampf erneut aufgegriffen. Dadurch entsteht ein motivischer Zusammenhang zwischen Intro und Kampfsituation, der die Immersion verstärkt.

![Projektansicht der Titelmusik in Reaper](img/schmiedpeter/Reaper_Titlemusik.png){width=80%}

Die Abbildung zeigt das Reaper-Projekt zur Titelmusik mit der Anordnung der Spuren und dem zeitlichen Aufbau des Intros.

- **Übergangsmusik**
Die Übergangsmusik markiert den dramaturgischen Wechsel vom Titelbildschirm zur ersten Gefahrenstufe des Bosskampfs. Ziel ist es, die Spannung innerhalb weniger Sekunden spürbar zu erhöhen, ohne einen hörbaren Bruch zwischen Intro und Kampfmusik zu erzeugen.
Als zentrales Motiv dienen drei tief gestimmte Glockenschläge (D–Bb–A), die als klangliches Warnsignal den Beginn der Konfrontation ankündigen. Die Tonfolge bleibt im Raum von D äolisch und betont mit dem Bb die kleine Sexte, wodurch die bedrohliche Grundstimmung konsequent erhalten bleibt. Die verwendeten Glockensamples (freesound.org, Big Ben 1988) wurden in Reaper klanglich bearbeitet und in das orchestrale Gesamtbild integriert [@freesound_signtoast_259965].

![Projektansicht der Uebergangsmusik in Reaper](img/schmiedpeter/Uebergangsmusik.png){width=80%}

Die Abbildung zeigt das Reaper-Projekt der Übergangsmusik und verdeutlicht den zeitlichen Aufbau vom Glockenmotiv zur Überleitung in die Bossmusik.

- **Bossmusik in mehreren Gefahrenstufen** (abhängig vom Bedrohungsgrad)
Die Bosskampfmusik wurde als dynamisches Layer-System konzipiert, bei dem sich die musikalische Intensität entsprechend des Kampfverlaufs stufenweise erhöht. **Danger Level 1** bildet dabei die klangliche Grundebene des gesamten Bosskampfs.

Ein rhythmisches Cello-Ostinato fungiert als zentrales Bewegungselement und erzeugt eine kontinuierliche Spannungswirkung. Ergänzt wird es durch tiefe Percussion mit langsamem, schwerem Puls, die den bedrohlichen Charakter der Situation akzentuiert. Im Hintergrund stützen tiefe Streicherflächen die düstere Grundatmosphäre.

Harmonisch bleibt die Gestaltung in **D äolisch** verankert, wodurch eine dunkle und bewusst instabile Klangfarbe erhalten wird. Die erste Gefahrenstufe ist kontrolliert und zurückhaltend angelegt, sodass bei zunehmender Bedrohung weitere Layer ergänzt werden können, ohne einen abrupten musikalischen Bruch zu erzeugen.

Für **Danger Level 2** und **Danger Level 3** wurde im Rahmen der Arbeit ein detailliertes musikalisches Konzept erstellt; eine vollständige klangliche Produktion beider Stufen konnte aus Zeitgründen jedoch nicht mehr abgeschlossen werden. Die technische Zustandslogik für die Aktivierung in Unreal wurde dennoch vorbereitet und in den Blueprint-Ablauf integriert (vgl. [Interaktive Musik in Videospielen](#sec-interaktive-musik)).

**Danger Level 2** erweitert die Grundstruktur von Level 1 um zusätzliche rhythmische und klangliche Ebenen. Das Cello-Ostinato bleibt als zentrales Motiv erhalten, wird jedoch durch aktivere Percussion, zusätzliche Streicherbewegungen und stärker eingesetzte tiefe Brass-Elemente ergänzt. Ziel dieser Stufe ist eine deutlich wahrnehmbare Intensivierung des Kampfgeschehens, ohne die musikalische Kontinuität zu unterbrechen.

**Danger Level 3** ist als maximale Eskalationsstufe konzipiert und für kritische Kampfmomente vorgesehen. In dieser Phase steigt die musikalische Dichte durch weitere orchestrale Layer, markantere Percussion, intensivere Brass-Akzente und einen breiteren Choreinsatz auf ihren Höhepunkt. Das Leitmotiv aus Danger Level 1 bleibt bewusst erhalten, um trotz maximaler Verdichtung ein konsistentes musikalisches Gesamtbild sicherzustellen.

- **Siegemusik (Victory Theme)**
Die Siegesmusik ist als kurzer Entspannungsmoment nach der Kampfspannung gedacht. Sie soll **Erleichterung**, **Triumph** und das **Ende der Gefahr** vermitteln.

Harmonisch wechselt sie von D äolisch nach **F-Dur** (relative Dur-Tonart zu D-Moll), wodurch der Eindruck von „Licht nach Dunkelheit“ entsteht. Als einfacher Verlauf wird **F – C – Dm – Bb** verwendet.

Die Instrumentierung bleibt weich und orchestral: **Hörner**, **Streicher**, **Chor**, **Harfe** und optional **Soft Piano**; Percussion entfällt. Die Melodie ist langsam und klar (z. B. **F–A–C–Bb / A–G–F**). Die Länge beträgt nur **wenige Sekunden** und markiert eindeutig den abgeschlossenen Sieg: Der Boss ist besiegt, der Kampf ist vorbei.

- **Niederlagenmusik (Defeat Theme)**
Die Niederlagenmusik soll **Scheitern**, **Hoffnungslosigkeit** und **Leere** vermitteln. Sie bleibt bewusst reduziert und kalt statt filmisch-dramatisch.

Harmonisch bleibt das Thema in **D-Moll** ohne Auflösung. Verwendet wird **Dm – Bb** oder in der minimalsten Form nur **Dm**.

Die Instrumentierung ist minimal: **Cello**, **tiefe Streicher** und sehr leiser **Chor**, ohne Percussion. Die Melodie bleibt langsam und fragmentarisch (z. B. **D–F–Bb / A**) und endet absichtlich offen. Die Länge beträgt nur **wenige Sekunden**; danach folgt der Game-Over-Screen.

Parallel dazu wurden die benötigten Soundeffekte definiert:

- **Schwerthit**
- **Magiebälle des Bosses** beim Abschuss

Die beiden Soundeffekte wurden mit zufallsbasierter Variation umgesetzt, wie es auch in vielen Spielen zur Vermeidung repetitiver Klangwahrnehmung eingesetzt wird (z. B. bei variierenden Treffersounds) [@collins_game_sound]. Der **Schwerthit** entstand aus einer eigenen Aufnahme eines dumpfen Schlags (Aufprall eines Handys auf eine gedämpfte Oberfläche) und wurde anschließend klanglich nachbearbeitet. Für die **Magiebälle** wurde als Ausgangsmaterial das Sprühgeräusch eines Deodorants verwendet und für den Projektilcharakter entsprechend angepasst.

Diese Struktur half dabei, Musik und Sound nicht isoliert, sondern als zusammenhängendes Feedback-System für den Spielverlauf zu entwickeln.

#### Exportieren und Einfügen in Unreal
Das Exportieren in Reaper war in der praktischen Umsetzung nicht besonders schwierig: Über **Rendern** wurde der jeweilige Titel ausgegeben, mit klarer Benennung und durchgängig im Dateityp **WAV**. Diese einheitliche Exportbasis erleichterte den anschließenden Import in Unreal deutlich.

Auch das Einfügen in Unreal war grundsätzlich unkompliziert. Eine wichtige Erkenntnis war jedoch, dass die Musik nicht ausschließlich im Blueprint einer einzelnen Map gesteuert werden sollte, da sie sonst beim Wechsel in die nächste Map abgeschnitten wurde. Die Lösung war eine eigene **Game Instance** für die Musiklogik, ergänzt durch zusätzliche **Blueprint Interfaces**, um Zustände und Trigger sauber zu übergeben.

![Sound-Logik in Unreal (Game Instance und Blueprint-Anbindung)](img/schmiedpeter/Sound_Unreal.png){width=80%}

Die Implementierung von Titelmusik, Übergangsmusik und Bossmusik **Danger Level 1** war vor allem eine Frage des richtigen Timings: Die jeweiligen Methoden mussten zum passenden Zeitpunkt ausgelöst werden. Für **Danger Level 2** und **Danger Level 3** wurde zusätzliche Logik eingebaut:

- **Danger Level 2:** Aktiv, wenn der Boss unter 50 % Leben ist **oder** der Spieler in Schlag- bzw. Schussreichweite ist.
- **Danger Level 3:** Aktiv, wenn **beide** Bedingungen gleichzeitig erfüllt sind.

![Bosskampf-Soundlogik mit Danger-Levels](img/schmiedpeter/Sound_Bosslogik.png){width=80%}

Die Sieges- beziehungsweise Niederlagenmusik wird beim Tod des Bosses beziehungsweise beim Tod des Spielers abgespielt.
