# Vererbung
Vererbung stellt ein zentrales Konzept in der OOP dar. Das 'Erben' beschreibt dabei, dass eine Klasse von einer anderen Klasse - der Basisklasse - Attribute und Methoden verwenden kann und diese in dem Bauplan der Klasse auch verfügbar sind. 

Möchte man nun nur bestimmte Methoden oder Attribute vererben, so kann man bestimmte Sichtbarkeiten für erbende Klassen bestimmen:
- public
- protected
- private

Einer der größten Vorteile der Vererbung ist es, das man für zukünftige Klassen einen 'Bauplan' vordefinieren kann. Auch wenn man später in der Entwicklung etwas hinzufügen oder entfernen möchte, hat man einen zentralen Ort (meist die Basisklasse) dafür der dann auch für alle erbenden Klassen gültig wird.

# Polymorphie
Objekte können nicht nur als Instanzen ihrer eigenen Klasse betrachtet werden, sondern auch als Instanzen übergeordneter Klassen oder Interfaces.
Polymorphie erlaubt es uns, Methoden abgeleiteter Klassen aufzurufen, obwohl wir nur eine Referenzvariable der Basisklasse zur Verfügung haben.
# Abstrakte Klassen
Eine abstrakte Klasse ist eine Klasse, die nicht instanziiert werden kann. Der Nutzen ergibt sich aus dem Konzept der Polymorphie: Man kann Methoden auf einem Objekt ausführen, ohne zu wissen, welche (abgeleitete) Klasse dahintersteckt. Dies ermöglicht eine flexible und effiziente Nutzung von Klassenhierarchien.

Im Kontext der Polymorphie könnte eine Methode wie tier.jump() aufgerufen werden, ohne zu spezifizieren, ob es sich um eine Katze, einen Hund oder ein anderes Tier handelt. Entscheidend ist, dass das Tier springen kann.

Ein Tier ist ein ideales Beispiel für eine abstrakte Klasse, da man in der Regel keine allgemeine Instanz von "Tier" erstellt, sondern spezifische Tiere wie Katzen, Hunde oder Hamster. Trotzdem haben alle Tiere gemeinsame Eigenschaften und Verhaltensweisen, wie die Fähigkeit zu springen (Methode jump()) oder Attribute wie height.

Um sicherzustellen, dass keine direkte Instanzierung der abstrakten Klasse Tier erfolgt, und gleichzeitig Methoden wie jump() oder Attribute wie height zur Verfügung zu haben, wird Tier als abstrakte Klasse definiert.

Eine konkrete Implementierung der abstrakten Klasse Tier könnte die Klasse Hund sein. Die Klasse Hund kann die Methode jump() anpassen, um spezifische Informationen zu berücksichtigen und die Funktionalität nach Bedarf zu modifizieren. Abgeleitete Klassen haben somit die Freiheit, Methoden für ihre spezifischen Anwendungsfälle zu überschreiben.

Regeln für eine abstrakte Klasse:

- Methoden können ohne Implementierung deklariert werden (abstrakte Methoden).
- Abgeleitete Klassen müssen abstrakte Methoden überschreiben (In machen Sprachen ist es nur optional).
- Die Klasse selbst muss als abstrakt deklariert werden (abstract class).
# Interfaces
In der Realität trifft man häufig auf die Situation, dass verschiedene Objekte ein ähnliches Verhalten zeigen sollen, aber eigentlich nicht sinnvoll in eine Vererbungslinie gebracht werden können. So eine Situation kann man mit Interfaces lösen. 

Ein Interface ist ein Vertrag der beschreibt, welche Methoden in einer Klasse vorhanden sein müssen. Möchte eine Klasse ein Interface implementieren, dann muss sie auch die im 'Vertrag' genannten Methoden anbieten. Dabei muss lediglich die Signatur übereinstimmen. 

Regeln für Interfaces: 
- Deklaration mit **interface**
- keine Attribute (Eigenschaften schon)
- Alle Elemente eines Interfaces sind implizit public
- Namenskonvention mit I als Präfix

# Interface vs. Abstrakte Klasse
- Abstract classes can have _constants, members, method stubs (methods without a body) and defined methods_, whereas interfaces can only have _constants_ and _methods stubs_.
- Methods and members of an abstract class can be defined with _any visibility_, whereas all methods of an interface must be defined as `public` (they are defined public by default).
- When inheriting an abstract class, a _concrete_ child class _must define the abstract methods_, whereas an abstract class can extend another abstract class and abstract methods from the parent class don't have to be defined.
- Similarly, an interface extending another interface is _not responsible for implementing methods_ from the parent interface. This is because interfaces cannot define any implementation.