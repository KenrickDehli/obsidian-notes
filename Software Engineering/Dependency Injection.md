In der herkömmlichen Objektorientierten Programmierung ist jedes Objekt dafür
Zuständig seine Abhängigkeiten (benötigte Objekte) zu erstellen und zu verwal-
ten. Das führt dazu, dass ein Objekt Wissen über seine Umgebung benötigt,
die es zur Erfüllung seiner eigentlichen Aufgabe gar nicht brauchen würde.
Des Weiteren führt dies führt oft zu direkten Abhängigkeitsbeziehungen und
unübersichtlichen Abhängigkeitsnetzen, die über mehrere Klassen verteilt sind.
Dependency Injection, auch häufig Inversion of Control genannt, bezeichnet ein
Entwurfsmuster, durch das es möglich ist, die Abhängigkeiten eines Objektes
zur Laufzeit an einem zentralen Ort zu hinterlegen. Das Objekt, das benötigt
wird, wird nicht vom initialisierten Objekt selbst erzeugt. Gemäß dem Single-Responsibility-Prinzip wird die Verantwortlichkeit “Aufbau eines Abhängigkeitsnetzes zwischen Objekten” aus den einzelnen Klassen in eine zentrale Komponente geführt.
DI überträgt die Verantwortung für das Erzeugen und Verwalten von Ob-
jekten an eine eigenständige Komponente, wie zum Beispiel ein DI Container.
Dadurch kann der Code des Objektes unabhängiger von seiner Umgebung sein.
Benötigte Referenzen können laut Martin Fowler in drei verschiedene Arten
gesetzt werden:
- Constructor Injection → Abhängigkeit wird im Konstruktor als Parameter
gesetzt und von einem Injizierer erstellt und injiziert.
- Interface Injection → Klassen implementieren ein Interface, das eine Me-
thode besitzt, die die Abhängigkeit injiziert.
- Setter Injection → Durch eine Methode innerhalb der Klasse, kann der
Injizierer eine Methode der Klasse aufrufen und die Abhängigkeit setzen.
Method Injection vs. Constructor injection → it depends, maybe Constructor
Injection for services used throughout the class and method injection for more
focused scenarios.
# Vorteile
- Klassen sind einfacher als isolierte Elemente zu testen.
- Durch durchgängige Implementierung der DI kann die Robustheit sowie die Wartbarkeit verbessert werden.
# Nachteile 
- Erhöhte Komplexität von Quellcode
- Mehr Kopf- und Planungsarbeit notwendig
- Meist anbindung einer DI Bibliothek notwendig → schwerer zu verstehen.
# DI Container
Ein DI Container ist ein Framework, um automatisch DI zu implementieren.
Der Container kreiert nicht nur ein Objekt einer spezifischen Klasse, sondern
injiziert auch alle Abhängigkeiten (bspw. durch einen Konstruktor, Property
oder Methode) zur Laufzeit und entsorgt diese zum richtigen Zeitpunkt. Da-
durch müssen Objekte nicht selber kreiert und verwaltet werden. Dabei sollte
jeder Container die folgende Lebenszyklen einer DI unterstützen:
- Register → Der Container muss wissen, welche Abhängigkeit zu instanzi-
ieren ist, wenn ein bestimmter Typ auftritt.
- Resolve → Der Container erstellt Objekte für uns, injiziert die Abhängig-
keiten und gibt das Objekt zurück.
- Dispose → Der Container verwaltet die abhängigen Objekte über den
gesamten Lebenszyklus.