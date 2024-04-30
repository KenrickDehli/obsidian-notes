SOLID sind fünf Prinzipien zum Entwurf und Entwicklung von wartbaren Soft-
waresystemen. Sie bestehen aus:
- Single Responsibility Principle (SRP)
- Open Closed Principle (OCP)
- Liskov Substitution Principle (LSP)
- Interface Segregation Principle (ISP)
- Dependency Inversion Principle (DIP)
# Single Responsibility Principle
Das SRP beschreibt, dass ein Modul nur einem Akteur gegenüber verantwortlich
sein sollte.
# Open Closed Principle
Das OCP beschreibt die Erweiterbarkeit von bestehender Software. Dabei sol-
len Softwareeinheiten (Module, Klassen, Methoden etc.) offen für Erweiterun-
gen, aber gleichzeitig auch verschlossen für Modifikationen sein (Verhalten sollte
sich nicht ändern). Vererbungen verhalten sich im Sinne des OCP, da sie einer-
seits offen für Erweiterungen sind, also es ist möglich neue Funktionalitäten
hinzuzufügen. Andererseits wird das Verhalten von vorhandenen Klassen nicht
geändert. Auch überschriebene Methoden verändern das Verhalten der Basis-
klasse nicht.
# Liskovsches Substitutionsprinzip
Das LSP besagt, dass ein Programm, das Objekte einer Basisklasse T verwendet,
auch mit Objekten der davon abgeleiteten Klasse S korrekt funktionieren muss,
ohne dabei das Programm zu verändern.
# Interface Segregation Prinzip
Das ISP beschreibt, dass zu große Schnittstellen in mehrere Schnittstellen auf-
geteilt werden sollen, falls implementierte Klassen Methoden haben, die sie
nicht benötigen. Nach der Anwendung des Prinzips müsste ein Modul, das ei-
ne Schnittstelle benutzt, nur diejenigen Methoden implementieren, die es auch
wirklich braucht. Der Vorteil davon sind schlankere Schnittstellen, die leichter
wartbar sind.
# Dependency Inversion Principle 
Das DIP beschreibt im wesentlichen, dass Module höherer Ebenen nicht von
modulen niedrigerer Ebenen abhängen sollten. Beide sollten von Abstraktionen
abhängen. Details sollten von Abstraktionen abhängen.
Dabei gilt, dass je niedriger das Modul ist, desto spezieller sind die Vorgänge, die
es definiert. In diesen Modulen werden Abläufe definiert, die meist in Abläufen
in höheren Ebenen benutzt werden.
Falls Module höherer Ebenen von Modulen niedrigerer Ebenen abhängen, en-
steht das Problem, dass die Änderungen in Modulen von niedrigeren Ebenen
unweigerlich zu Änderungen in Modulen von höheren Ebenen führen. Dadurch
entsteht eine erhöhte Kopplung von modulen, welche Änderungen in Architektur
und Design unnötig verkomplizieren. Der Lösungsansatz dafür ist die Invertie-
rung der Abhängigkeit, indem das Modul der höheren Ebene eine Schnittstelle
definiert, mit der es arbeitet und die Module niedrigerer Ebenen diese realisie-
ren.