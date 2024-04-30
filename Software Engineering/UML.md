Die Unified Modeling Language, kurz UML ist eine Sprache zur Modellierung
von Softwareprojekten. Ziel der modellierung ist es, nicht nur den Aufbau einzel-
ner Klassen zu modellieren, sondern auch deren Beziehungen zu einander. Die
drei Arten von Beziehung sind:
• Generalisierung → Vererbungsbeziehung
• Assoziation → allgemeine Beziehung zwischen Klassen
• Abhängigkeiten → Nutzungsbeziehung

UML-Diagramme sind bei der Architektur von [[OOP|objektorientierten]] Systemen zusammen mit [[Entwurfsmuster|Design Patterns]] ein mächtiges Werkzeug.

# Assoziationen
Darstellung von strukturellen Beziehungen zwischen Klassen → Klassen kennen
und nutzen sich, ohne direkt voneinander zu erben. Dabei gibt es drei Arten
von Assoziationen:
• Einfache Assoziation: gleichberechtigte Beziehung zwischen zwei Klassen.
Sie arbeiten miteinander und trennen sich wieder.
• Aggregation: Beschreibt eine Teil-ganzes Beziehung. Es handelt sich dabei
um eine symbolhafte Darstellung
• Komposition: Teil-ganzes Beziehung, mit einer Aussage der Lebenszeit
der Objekte: Wenn das Ganze ”stirbt”, dann auch seine Teile. Folglich
steht auf der Seite des Aggregats als Kardinalität immer eine 1!
