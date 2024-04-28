**Lösungen siehe PDF**

# Theoretische Grundlagen

## 1.1

*Zeige mir die Adressen aller Personen an, die in Frankfurt wohnen.*
## 1.2
- Lies  den ersten Satz der Datei ADRESS
- Wiederhole solange das Ende noch nicht erreicht wurde:
	-  Falls der Datensatz den Namen "Sean Connery" besitzt, kopiere ihn in ERGEBNIS
	- Lies den nächsten Datensatz von ADRESS
- Gib die Daten der Datei ERGEBNIS aus

## 1.3
1. Die "Autor"-Spalte hat potentiell den gleichen Autor wie in Tabelle 1.1 bspw. "Beutelspacher"
2. Dasselbe gilt für die Spalten "Titel" und "Verlag"

## 1.4
Ich würde empfehlen die zwei Spalten Autor und Titel in eine Datei zu schreiben und die Verlag-Spalte in eine zweite Datei zu speichern. 

## 1.5
a)
1. Ein Mitarbeiter löscht einen Eintrag, während ein anderer diesen nur verändern möchte. 
2. Mehrere Mitarbeiter verändern den gleichen Eintrag → welcher ist nun gültig?
b)
-  Es darf nur ein Mitarbeiter gleichzeitig an der Datei arbeiten 
-  Es gibt Mitarbeiter mit nur lesenden Rechten und Mitarbeiter mit schreibenden Rechten
-  Echtzeit-Synchronisation
## 2.2

Titel | Künstler | Länge | Album |

## 2.3 
Die gestellte Anfrage widerspricht unserer Charakterisierung rel. Datenbanksysteme, da hier nicht explizit nach einem Attribut eines Objekts gefragt wird. Die korrekte Anfrage müsste heißen: *Gebe mir die Einträge von ADRESSE, bei denen der Vorname = Karl und der Nachname = Engels lautet*

aus der Lösung: Bilde aus der Tabelle PERSON die Teiltabelle, die nur den Satz von Karl
Engels enthält (das werden wir später eine Restriktion nennen) und erstelle
aus dieser Tabelle eine „schmalere“ Tabelle, die nur noch aus dem Attribut
„Telefonnummer“ besteht (das werden wir später eine Projektion nennen).

## 3.1
a)
- Id
- Bestelldatum (vorausgesetzt eine Bestellung pro Tag)
b)
Definitiv für die Id. Schon an der Beispieltabelle sieht man, dass die anderen Attribute nicht einzigartig sind, was gegen unseren Anspruch an einen Primärschlüssel verstößt. Auch das Bestelldatum kann potentiell mehrfach belegt sein, da ein Kunde zwei Bestellungen an einem Tag aufgeben kann. Auch vor dem Aspekt der Integrität scheitern die anderen Attribute im Vergleich zur Id. So kann sich bspw. eine Kunden Id im Laufe der Jahre verändern oder auch die LfdNr. Mit der Id kann man die Einzigartigkeit, sowie die langfristige Integrität des Primärschlüssels gewährleisten. 
## 3.2
Ein Datensatz der Tabelle BESTELLUNGEN sollte:
- eine eindeutige ID vorweisen
- Jeder Attributwert in der Spalte KundId der Tabelle BESTELLUNGEN muss
auch in der Spalte Id der Tabelle KUNDEN vorkommen. → Analog zu ArtikelId
- Die Lfd muss bei Bestellung inkrementiert werden. 
- Der Attributwert für KundeId  darf sowohl in der Tabelle KUNDE als auch in der Tabelle BESTELLUNGEN nicht leer sein. → Analog für ArtikelId
- Der Attributwert für Bestelldatum, Menge, LfdNr darf nicht leeer sein. 
- LfdNr muss >= 0 sein. 
## 3.3
es ist a)

## 4.1 
a) 
A X B = {(1, eins), (2, eins), (3, eins), (1, zwei), (2, zwei), (3, zwei)}
b) 
Ja, R ist eine Relation , da R eine Teilmenge von A X B ist: R:= {(1,eins),(2,zwei)} ⊆ A X B.
c) 

| Zahl | Name |
| ---- | ---- |
| 1    | eins |
| 2    | zwei |
d) 
soviel, wie die Kardinalität des kartesischen Produkts ergibt: 
$$
6\times4\times2 = 48 
$$

## 5.1
a)
Gebe mir alle ARTIKEL WHERE Bestellungen.ArtikelId = Artikel.id

b)
PROJECT ( ARTIKEL EQUIJOIN BESTELLUNGEN ON Bestellungen.ArtikelId = Artikel.Id ) (Alle Attribute von ARTIKEL)

c)
PROJECT(Artikel x Bestellungen WHERE Artikel.id = Bestellungen.ArtikelId) (*schreibe hier alle Attribute von Artikel auf mit komma als Separator*.)

## 5.2
Kardinalität = 300 
Grad = 9

## 5.3
Der einzig sinnvolle natural join zwischen Artikel und Artikelgruppe ist der einfache natürliche join, da man nur ein Paar miteinander verbinden muss. Der natürliche join beschreibt die sequentielle Ausführung von Product (kartesisches Produkt), Restriction (Restriktion) und Project (Projektion). Der letze Schritt deshalb, weil man in der Darstellung Spalten mit den gleichen Informationen vermeiden will. 
1. PROJECT(RESTRICTION(PRODUCT(Artikel, Artikelgruppe), Artikel.grupId = Artikelgruppe.id)) (alle Attribute von Artikel)
2. Artikel NATURAL JOIN Artikelgruppe ON Artikel.grupID = Artikelgr.id