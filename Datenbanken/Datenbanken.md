# Theoretische Grundlagen 

[[TheoretischeGrundlagen.pdf#page=13&selection=7,0,37,43|Zusammenfassung Kapitel 1 ]]
[[TheoretischeGrundlagen.pdf#page=18&selection=47,0,47,15|Zusammenfassung Kapitel 2]]
[[TheoretischeGrundlagen.pdf#page=32&selection=7,0,7,15|Zusammenfassung Kapitel 3]]
[[TheoretischeGrundlagen.pdf#page=45&selection=68,0,68,15|Zusammenfassung Kapitel 4]]
[[TheoretischeGrundlagen.pdf#page=62&selection=20,0,20,15|Zusammenfassung Kapitel 5]]
## Random Gedanken
- Hinter Relationen versteckt sich die relationale Algebra
- Alle Relationen geben Relationen zurück. Analog für Tabellen
- Eine Datenbanksprache muss die grundlegenden Operatoren abbilden können. 
## Kapitel 1
Forderung an Datenbanken: 
- Die Daten müssen persistent gespeichert werden
- Zugriff auf die Daten nach komfortable Datensuche → Sortierungen, Gruppierungen
- Datenbank soll man durchsuchen und verändern können → [[TheoretischeGrundlagen.pdf#page=10&selection=117,0,132,69|Definition, page 10]]
- Redundanz vermeiden, indem Einträge mit ähnlicher Eigenschaft auf eine Verweisen →  [[TheoretischeGrundlagen.pdf#page=11&selection=37,0,40,7| Beispiel Redundanz]]
- Dateninkonsistenz vermeiden

Forderung an Datenbanksysteme:
- Ein Datenbanksystem muss für einen Mehr-Benutzer Betrieb ausgelegt sein
## Kapitel 2 - Relationen und andere Datenbanksysteme
*Tabellen sind eine Veranschaulichung von Funktionen (Funktionen sind auch Relationen). In einer Tabelle stehen die Werte, die zu einer Funktion (oder Relation) gehören.*

Entwurfsfehler: 
-  Mögliche Datenredundanz 

Bei dem Entwurf von Tabellen/Datenbank stellt man sich folgende Frage: **_Welche Attribute haben die Datensätze?_**

**Definition**
	*Gegeben sei eine Menge von Objekten. Ein Attribut ist eine Eigenschaftsart,
	die alle Objekte dieser Menge besitzen. Jedem Objekt dieser Menge ist genau
	ein Wert dieses Attributs, der sogenannte Attributwert zugeordnet. Ein
	Attribut muss einen Namen haben, den sogenannten Attributnamen. Dieser
	Attributname muss unter allen Attributnamen der betrachteten Objekte ein-
	deutig sein.*

*Eine Menge von Objekten, die durch die Werte einer einheitlichen Attributkombination vollständig und eindeutig beschrieben werden, heißt Relation.

- Datensatz = Zeile in der Tabelle, die ein Objekt repräsentiert. 
- Spalten = Attribute
- Tabellen = konkrete Beschreibung von Relationen mithilfe der einheitlichen Kombination von Attributen 

Der Benutzer einer relationalen Datenbank sieht die Daten nur in Form von
Tabellen. Alle Operationen, die dem Benutzer einer relationalen Datenbank
zur Verfügung stehen (z. B. zum Einfügen, Ansehen, Ändern und Löschen von
Daten), operieren auf der Basis von Tabellen. Sie generieren neue (Teil-)Tabel-
len, löschen diese usw.

## Kapitel 3 - Eine Beispieldatenbank
Das **relationale Modell** ist durch folgende Punkte charakterisiert: 
1. Die Daten können nur in Form von Tabellen betrachtet und verändert
werden. Das wird oft der strukturelle Aspekt genannt.
2. Alle Operatoren, die dem Benutzer zur Manipulation von Daten zur Ver-
fügung stehen, operieren grundsätzlich nur auf Tabellen und ergeben
auch wieder neue Tabellen. Ein relationales System enthält mindestens
die Operatoren RESTRICT, PROJECT und JOIN. Man nennt diesen
zweiten Punkt den manipulativen Aspekt des relationalen Modells.
(Dieser zweite Punkt wird im fünften Kapitel dieses Heftes behandelt.)
3. Tabellen müssen gewissen Integritätsbedingungen genügen. (Dieser drit-
te Punkt wird bei der Vorstellung unserer Beispieldatenbank erläutert
und im sechsten Kapitel genau diskutiert.)

Was benötigt man also für eine **Tabelle**? 
### **Primärschlüssel**
Ein Primärschlüssel sichert die Integrität der Beziehungen zwischen Tabellen. **Ein Attribut oder eine Kombination** von Attributen einer Tabelle, das bzw. die für jeden Satz dieser Tabelle eindeutig ist. 

Kriterien für einen guten Primärschlüssel: 
- Keine für den Benutzer bedeutenden Informationen, da sich benutzerrelevante Daten während der Lebenszeit eines Datenobjekts [[TheoretischeGrundlagen.pdf#page=21&selection=71,44,78,0|verändern]]. Ein Primärschlüssel sollte also **konstant** sein. 
- Struktur des Primärschlüssels sollte möglichst einfach sein. 

### Constraints
Beschreiben die Bedingungen an die Daten einer Datenbank. Jeweils für ein Attribut (Spalte) einer Tabelle definieren. 
### Attribute
*Zusätzlich zu den Begriffen Attributwert und Attributname (siehe Kapitel 2)
definieren wir jetzt noch für Attribute einer Tabelle einer relationalen Daten-
bank den Begriff des Attributtyps. Der Attributtyp ist der Datentyp, der für
die Variable vorgesehen ist, auf der die entsprechenden Attributwerte gespei-
chert werden sollen.*

Default-Wert = Wert, der standardmäßig vom (DM-)System zugewiesen wird, falls der Benutzer keine Wertzuweisung vornimmt.

#### Nullwerte
NULL bedeutet das kein (Werte-)Element aus dem Wertebereich ausgewählt wurde. Dies entspricht dann kein Eintrag. Dies führt allerdings nicht in der Entwurfsphase, sonder später zu Problemen, da man bei jeder Abfrage den NULL-Wert in seine Query [[TheoretischeGrundlagen.pdf#page=25&selection=62,0,72,21|miteinbeziehen]] muss. 

### Integrität
Die Integrität einer relationalen Datenbank wird durch die Erfüllung der
folgenden drei Bedingungen definiert:
1. Jeder Satz einer Tabelle hat einen eindeutigen Primärschlüsselwert. Man
nennt diese Bedingung auch Entity-Integrität.
2. Zu jedem Fremdschlüssel in einer Tabelle T1 gibt es einen identischen
Schlüsselwert in einer anderen Tabelle T2, die dafür beim Anlegen von T1
festgelegt wurde. Man nennt diese Bedingung auch **referentielle
Integrität.**
3. Alle weiteren Bedingungen, die beim Anlegen einer Tabelle festgelegt wur-
den, sind erfüllt. Mit anderen Worten: Die restlichen Constraints sind er-
füllt.

## Kapitel 4 - Tabellen und Relationen
### Kartesisches Produkt vs. Relation
Ein Kartesisches Produkt betrachtet **alle** Kombinationen der Elemente von bestimmten Mengen. Die Relation ist dabei eine Teilmenge des kartesischen Produkts und betrachtet diejenigen Elemente, die für uns Relevant sind. Die Tupelkombinationen stehen bei einer Relation  zueinander in Beziehung. Man gibt dann dieser Beziehung den Namen der Relation.
[[TheoretischeGrundlagen.pdf#page=38&selection=114,0,114,63|Definition -  Tabellendarstellung.]]
[[TheoretischeGrundlagen.pdf#page=38&selection=116,0,164,0|Definition - Relation]]
[[TheoretischeGrundlagen.pdf#page=39&selection=152,0,152,10|Beispiel Relation]]
### Datenbankrelation
*Datenbankrelationen sind Mengen.* → Erinnerung: Mengenelemente sind wohl-unterschieden.
- [[TheoretischeGrundlagen.pdf#page=41&selection=97,0,156,20|Definition - Datenbankrelation]] → Namen der Spalten A1 bis An sind eindeutig und verschieden.
**Nach nach unserer Definition ist jede Spalte eine Menge!**
- [[TheoretischeGrundlagen.pdf#page=41&selection=25,0,25,42|Bsp. Definition einer DB-Relation.]]
- [[TheoretischeGrundlagen.pdf#page=42&selection=39,0,136,12|Warum NULL in der Relationensprache Unsinn ist.]]
#### Datenbankrelation vs Datenbanktabelle
Eine Datenbankrelation ist potentiell unendlich wobei die Datenbanktabelle eine Darstellung der DB-Relation sein soll und nur endlich viele Elemente hat. Man kann sagen, durch die Präsentation einer Datenbankrelation durch eine Datenbanktabelle geht eine gewisse Abstraktion verloren. 

Verwendet man nun bspw. SQL, so kann man mit einer Anfrage gleiche Elemente erfragen. Dies verstößt allerdings gegen die Eigenschaft von Mengen und deren Elementen. Also sollte man sich dies bei Anfragen an bspw. SQL in Erinnerung rufen und einen Befehl wie DISTINCT verwenden um mehrfach vorkommende Tabellenzeilen zu verhindern (Sonst verschwindet auch die eindeutige Zuordnung).

- [[TheoretischeGrundlagen.pdf#page=44&selection=77,0,81,46|Ergebnis von Abbildungen und Operatoren.]]
- [[TheoretischeGrundlagen.pdf#page=45&selection=83,0,96,45|Definition - Kardinalität]] → Anzahl der Elemente der Relation.
- [[TheoretischeGrundlagen.pdf#page=45&selection=98,0,108,44|Definition - Grad]] → Anzahl der Spalten.

### Das relationale Modell
[[TheoretischeGrundlagen.pdf#page=45&selection=23,0,66,38|Definition - Das relationale Modell]]
1. strukturelle Aspekt
2. manipulativer Aspekt
3. Integrität

## Kapitel 5 - Relationale Operatoren 
### Warum Operatoren?
Zur Vermeidung von Datenredundanzen verteilt man die gewünschten Daten auf mehrere Tabellen. Um diese wieder auf verständliche Weise zusammenführen zu können, benötigt man Operatoren. Allerdings sind relationale Operatoren auch nützlich für "[[TheoretischeGrundlagen.pdf#page=61&selection=68,0,100,10|theoretische Zwecke]]":
[[TheoretischeGrundlagen.pdf#page=47&selection=85,0,113,3|Definition - Rel]]
[[TheoretischeGrundlagen.pdf#page=48&selection=143,0,163,4|Definition - typ- und union-kompatibel]] → 2 Teilmengen aus gleichem Kreuzprodukt
[[TheoretischeGrundlagen.pdf#page=48&selection=52,1,111,1|Definition - Union]] → UNION(R,S) Vereinigungsmenge der Relationen R und S
[[TheoretischeGrundlagen.pdf#page=49&selection=32,0,87,1|Definition - Intersection]] → INTERSECTION(R,S) Schnittmenge der Relationen R und S
[[TheoretischeGrundlagen.pdf#page=49&selection=128,0,199,2|Definition - Difference]] → DIFFERENCE(R,S) Differenz der Relationen R ohne S
- Union, Intersection und Difference sind nur möglich wenn R und S auch Teilmengen desselben kartesischen Produkts sind!
[[TheoretischeGrundlagen.pdf#page=51&selection=177,0,266,24|Definition - Product]] → PRODUCT(R, S) das kartesische Produkt aus den Relationen R und S
- Das Kartesische Produkt zu bilden scheint auf den ersten Blick sinnlos, da man ja alles mit allem mischt. Allerdings stellt das Produkt die Basis der weiteren Operatoren dar, für die man eine gewisse typ- und unions-Kompatibilität benötigt.
 [[TheoretischeGrundlagen.pdf#page=53&selection=22,0,96,1|Definition - Restrict]] → Teilmenge einer Relation mit Elementen, die eine gewisse Bedingung erfüllen. Analog zu SQL WHERE
 [[TheoretischeGrundlagen.pdf#page=53&selection=122,0,139,16|Beispiel - Definierte Restriktion]]
 [[TheoretischeGrundlagen.pdf#page=55&selection=48,0,85,19|Definition - Projektion]] → PROJECT(R) projiziert eine Relation auf eine Menge und macht deren Elemente dadurch "schmaler". 
 [[TheoretischeGrundlagen.pdf#page=56&selection=4,1,13,10|Beispiel - Projektion]]
 [[TheoretischeGrundlagen.pdf#page=58&selection=47,1,196,1|Definition - Natural Join, einfache Form]] → nur über ein Attributpaar, R NATURAL JOIN S R.Ai = S.Bj. Reihenfolge dabei: 
 1. Produkt
 2. Restriktion
 3. Projektion
[[TheoretischeGrundlagen.pdf#page=58&selection=200,0,200,49|Beispiel - Natural Join einfache Form]]
[[TheoretischeGrundlagen.pdf#page=59&selection=77,0,77,51|Definition - Natural Join, allgemeine Form]] → Gruppe von Attributpaaren erlaubt
[[TheoretischeGrundlagen.pdf#page=60&selection=112,0,112,14|Definition - Theta Joins]] → Theta bedeutet hier, ein beliebiger Vergleichsoperator aus der Menge {<, <=, =, !=, >, >=}
EQUIJOIN → Natural Join ohne abschließende Projektion
[[TheoretischeGrundlagen.pdf#page=61&selection=25,0,37,1|Beispiel - Divide]]









