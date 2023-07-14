# Rubik's Cube Projekt mit Three.js
Dieses Projekt wurde von Ayman AbouHashem und Bassel Samo entwickelt, um einen interaktiven Rubik's Cube mithilfe der Three.js-Bibliothek zu erstellen.

## Vorraussetzungen
Um das Projekt auszuführen, brauchen Sie einen Webbrowser, der WebGL unterstützt. Z.B. Google Chrome, Mozilla Firefox oder Microsoft Edge.

## Installation
Das Projekt können Sie direkt im Browser ausgeführen. Stellen Sie sicher, dass Sie eine Internetverbindung haben, um die Three.js-Bibliothek von einer CDN-Quelle zu laden.

## Ausführen des Projekts
Öffnen Sie einfach die Datei index.html in einem Webbrowser.

## Funktionalitäten
Der Rubik's Cube kann interaktiv mit der Maus gedreht werden. Darüber hinaus sind folgende Funktionen implementiert:
Sie können den Rubik’s Cube interaktiv mit der Maus drehen. Darüber hinaus haben wir die folgenden Funktionen implementiert:

•	Zufällige Farbänderung des Cubelets durch Drücken der Leertaste.
•	Cubelet-Bewegungen durch den Pfeiltasten (links und rechts)

## Code-Erklärung
Der Code haben wir in einem HTML-Datei geschrieben und dazu ein JS Skript addiert und Three.js-Bibliothek verwendet, um den Rubik's Cube zu erstellen und zu rendern.

### HTML-Struktur
Die HTML-Datei enthält ein Canvas-Element, in dem der Rubik's Cube gerendert wird. Es gibt auch ein Div-Element mit der ID "timer" für eine optionale Timer-Anzeige, jedoch haben wir keine Implementierung dazu geschafft.

### JavaScript-Code
Der JavaScript-Code beginnt mit dem Import der benötigten Module, darunter die OrbitControls und der GLTFLoader von Three.js.

Der Code erstellt eine Three.js-Szene, eine Kamera und einen Renderer. Die Kamera haben wir durch x-, y- und  z-Koordinate so positioniert, dass der Cube sichtbar ist. Wir haben  auch eine Instanz der OrbitControls verwendet, um die interaktive Steuerung des Cubes zu ermöglichen.

#### Erstellung eines Cubelets
Die Funktion createCubelet wird verwendet, um ein einzelnes Würfelelement (Cubelet) zu erstellen. Es verwendet die BoxGeometry und MeshBasicMaterial von Three.js, um die Geometrie und das Material des Cubelets festzulegen. Der Code erstellt auch Kanten (Edges) für das Cubelet, um seine Struktur sichtbar zu machen.

#### Erstellung des Rubik's Cube
Den Rubik's Cube haben wir durch eine dreidimensionale Matrix von Cubelets repräsentiert. Wir haben eine Schleife verwendet, um alle Cubelets zu erstellen und ihre Positionen und Farben festzulegen. Die Positionen der Cubelets sind basierend auf ihrer x-, y- und z-Koordinate festgelegt, und die Farben werden aus dem vordefinierten Farbarray ausgewählt.

#### Interaktion mit dem Rubik's Cube
Wir haben nur das erste Cubelet aus dem Cubelet-Array ausgewählt. Ein Event-Listener für die Leertaste, die Pfeiltasten (links und rechts) und den Mausklick auf das Cubelet haben wir eingefügt. Bei Drücken der Leertaste wird eine zufällige Farbe für das Cubelet gesetzt, bei den Pfeiltasten können Sie das Cubelet horizontal verschieben, und beim Mausklick auf das Cubelet kriegen Sie eine Nachricht in der Konsole.

#### Animation
Wir haben eine animate-Funktion definiert, die den Render-Loop für die Szene steuert. Sie wird mithilfe von requestAnimationFrame aufgerufen und rendert die Szene mit dem aktualisierten Kamerablickwinkel. In diesem Codebeispiel haben wir einige Zeilen auskommentiert, die die Cubelets rotieren lassen würden. Wenn Sie diese Zeilen wieder aktivieren, wird der Rubik's Cube animiert.

## Anpassung des Codes
Im Vergleich zu dem auskommentierten Code haben wir einige Zeilen geändert, um die Darstellung und Struktur des Rubik's Cube zu verbessern. Hier sind die Abschnitte, die wir hinzugefügt, und ihre Funktionen:

#### Gruppierung von Cubelets und Kanten
In der Funktion createCubelet haben wir eine THREE.Group erstellt, um das Cubelet-Mesh und die Kanten zusammen zu gruppieren. Dadurch wird sichergestellt, dass das Cubelet und die Kanten gemeinsam transformiert werden und ihre relative Position beibehalten.

#### Anpassung der Rubik's Cube-Erstellung
Statt der vorherigen Methode, die den Cube durch die Anzahl der Kanten pro Seite aufteilte, haben wir nun eine dreidimensionale Matrix von Cubelets erstellt. Jedes Cubelet erhält eine bestimmte Position basierend auf den Koordinaten x, y und z. Die Farbe jedes Cubelets wird aus dem Farbarray entsprechend der Position bestimmt.

#### Entfernung der Mausklick-Interaktion
Die Mausklick-Interaktion mit dem Cubelet haben wir im aktualisierten Code auskommentiert. Der entsprechende Event-Listener haben wir auch entfernt. Dies kann angepasst werden, um individuelle Aktionen für den Mausklick auf ein Cubelet hinzuzufügen.

#### Weitere Anmerkungen
Einige andere Zeilen aus dem letzten Code, die wir für die Cube-Rotation verwendet haben, haben wir auskommentiert. Diese Zeilen können bei Bedarf wieder aktiviert werden, um eine Animation des Rubik's Cube zu ermöglichen.

