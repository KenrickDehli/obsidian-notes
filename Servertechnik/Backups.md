# 3-2-1
Gilt als goldene Regel der Datensicherheit. Drei kopien von Daten auf zwei ver-
schiedenen Speichermedien, von denen ein Datenträger davon an einem anderen
Standort gesichert ist.
## Vollsicherung

Die Vollsicherung bezeichnet die Speicherung eines kompletten Abbildes
der Daten. Das kann bspw. die Sicherung einer kompletten Festplatte sein
oder die Sicherung eines kompletten Ordners mit den entsprechenden
Unterordnern und Dateien.

## Differenzielle Sicherung

Der aktuelle Datenbestand wird mit der letzten Vollsicherung verglichen
und es werden alle Daten gesichert, die sich nach der letzten
Vollsicherung geändert haben. Für eine Rekonstruktion braucht man also
die letzte Vollsicherung und die letzte differenzielle Sicherung.

## Inkrementielle Sicherung

Es wird immer nur das gesichert, was sich nach der letzten Vollsicherung
und den anschließenden inkrementellen Sicherungen verändert hat. Für
eine Rekonstruktion braucht man also die letzte Vollsicherung und alle
weiteren inkrementellen Sicherungen danach.

## Revisionssicherheit

Revisionssicherheit betrifft hauptsächlich solche Daten, die auf Grund
rechtlicher oder gesetzlicher Anforderungen unveränderbar
aufbewahrungspflichtig und -würdig sind. Relevant dafür ist:

-   Vollständigkeit → kein Datenverlust (auch Metadaten)

-   Schutz vor Veränderung und Verfälschung

-   Sicherung vor Verlust → Dauerhaft

-   Nutzung nur durch Berechtigte

-   Dokumentation des Verfahrens → Archivierungsverfahren um bspw. ein
Archiv reibungslos migrieren zu können.

### Lebensdauer Speichermedien

![[Speichermedien.png]]
