Muster für den Entwurf sind bewährte Lösungsvorschläge für bestimmte Prob-
lemstellungen, die beim Entwurf von Systemen beachtet werden sollten, da sie
sich bereits in mehreren Systemen bewährt haben. Grundlage um Entwurfsmuster richtig Anwenden zu können sind [[OOP#^4ee3d2|Interfaces]] und [[OOP#^0e8954]|abstrakte Klassen]].
# Singleton
Es soll eine Klasse geben, von der sichergestellt werden muss, dass nur eine
einzige Instanz von ihr existiert. Für das Erzeugen der einzigen Instanz soll die
genannte Klasse selbst verantwortlich sein. Merkmale:
• privater Konstruktor
• Alle Objekte die mit dem Singleton arbeiten möchten, erhalten eine Ref-
erenz auf das Objekt
• statisches Attribut vom eigenen Klassentyp

![[Singleton.png]]
# Observer 
Ändert sich der Zustand eines Objekts, sollen alle von diesem Objekt abhängigen
Objekte benachrichtigt werden, so dass eine Aktualisierung dieser Objekte au-
tomatisch eingeleitet werden kann. Die Menge der Objekte, die bei einer Zus-
tandsänderung benachrichtigt werden sollen, soll dynamisch veränderbar sein,
d. h., abhängige Objekte können zu dieser Menge hinzukommen und zu einem
späteren Zeitpunkt auch wieder entfernt werden.
Das Beobachter-Muster soll es erlauben, dass ein Objekt abhängige Objekte von
einer Änderung seines Zustands informiert, so dass eine Aktualisierung automa-
tisch eingeleitet werden kann. Merkmale:
• Ein Daten-haltendes Objekt (Observable/Publisher), dessen Daten, also
Zustand sich ändern können
• Interessenten (Observer/Subscriber) für die gekapselten Daten, die auf die
Änderungen reagieren wollen.
• aktualisieren() Methode in Observer Klasse→ Observer übergibt sich bei
Aufruf selbst (oder nicht... im Unterricht jedenfalls nicht).
• gibZustand()/Notify(), Anmelden(Observer) und Abmelden(Observer) Meth-
ode bei Observable Klasse.
Der Observer registriert sich bei dem Observable Objekt und wenn sich
der Zustand des Observables ändert, dann werden diese benachrichtigt, und
anschließend aktualisieren die angemeldeten Observer die Veränderung.

![[Observer.png]]
# Factory
Das Factory (Method) Pattern wird meist bei wiederverwendbaren Anwendun-
gen angewendet, wie z.B. bei der Entwicklung von Frameworks. Hier sollen nur
Basisklassen beinhaltet sein (bspw. abstrakt/Interfaces) und das bedeutet, dass
eine wiederverwendbare Anwendung Objekte nicht hart codiert erzeugen kann,
da sie die eigentlichen Klassen ja gar nicht kennt. Diese Klassen sollen erst zur
Laufzeit von dem Programm, das die wiederverwendbare Anwendung benutzt,
zur Verfügung gestellt werden. Wir wollen also kontrollieren, wo unsere Objekte
erzeugt werden. Das Fabrikmethode-Muster soll es erlauben, dass die Erzeu-
gung einer konkreten Instanz in der Methode einer Unterklasse gekapselt wird
und dabei wird die Erzeugung des Objekts verlagert bzw. delegiert. Merkmale:
• höhere, abstrakte Ebene mit Erzeuger Klasse und Produkt Klasse
4• abstrakte Fabrikmethode in der Objekte, vom Typ Produkt, erzeugt und
als Ergebnis zurückgegeben werden.
• tiefere, konkrete Ebene mit konkreten Erzeugern und konkreten Produk-
ten

![[Factory.png]]