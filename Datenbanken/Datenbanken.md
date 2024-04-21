# Theoretische Grundlagen 

[[TheoretischeGrundlagen.pdf#page=13&selection=7,0,37,43|Zusammenfassung Kapitel 1 ]]
[[TheoretischeGrundlagen.pdf#page=18&selection=47,0,47,15|Zusammenfassung Kapitel 2]]
[[TheoretischeGrundlagen.pdf#page=32&selection=7,0,7,15|Zusammenfassung Kapitel 3]]

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


