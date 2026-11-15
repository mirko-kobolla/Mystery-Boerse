# Ideen und Änderungen

Dieses Dokument hält die umgesetzten Spielentscheidungen und spätere Ideen fest. Neue Einträge werden chronologisch ergänzt.

## Umgesetzt am 14.11.2026

- Startkapital je Depot auf 20.000 € gesetzt; alle acht Startkurse auf 5.000 € und der Mindestkurs auf 200 € gesetzt.
- Die bisherigen Titel durch die acht deutschen Unternehmen aus dem Spielprinzip ersetzt.
- Prozentuale Kurs- und Vermögensanzeigen durch absolute Eurobeträge ersetzt.
- Die acht geheimen Kursregeln als geordnete Berechnung bei Rundenbeginn umgesetzt. Der zufällige Telekom-Geheimnisstatus wird auf der Host-Tafel durch 🔒 kenntlich gemacht; die Regeln selbst erscheinen nicht in der Spieloberfläche.
- Die Host-Tabelle durch ein 4×2-Kartenraster mit individuellem SVG-Kursverlauf und Klassen-Handelszahlen ersetzt.
- Host-Steuerungen zum Pausieren/Fortsetzen und vorzeitigen Beenden ergänzt; Clients können während der Pause nicht handeln.
- Neustart-Schaltfläche nach Spielende und im Verbindungsfehler-Fall ergänzt, damit die Anwendung ohne manuelles Schließen des Tabs erneut gestartet werden kann.
- Die PeerJS-Kommunikation zwischen Host und Clients beibehalten.
- Im Repository existiert keine `index.html`; die bestehende Anwendung liegt in `boersen-spiel.html`, die deshalb angepasst wurde.

## Umgesetzt am 15.11.2026

- Die Kursregeln für Cyber Securit, Hochtief Bauwesen und Rhein-Main Bank AG auf die festgelegten prozentualen Änderungen umgestellt; prozentuale Kursänderungen werden auf volle Euro gerundet.
- Die Alt-Entertaiment-Kurve bildet das W-Logo über sechs Abschnitte mit je vier Runden pro Abschnitt nach. Die bisherigen Bewegungen von −500 € und +700 € bleiben dabei erhalten.
- Die Verdecken-Funktion ergänzt: Jeder Spieler kann einmal pro Partie eine Aktie für die laufende und die folgende Runde verdecken. Kurs und eigener Bestand der Aktie sowie die Vermögenssummen der Clients bleiben während aktiver Verdeckungen verborgen; der Handel bleibt möglich.
- Eine Live-Rangliste mit Gesamtvermögen in der Host-Ansicht ergänzt, die sich erst nach jeder Runde aktualisiert. Während einer Verdeckung sind dort nur die Platzierungen sichtbar; bei Spielende werden in der Siegerehrung immer alle Endvermögen offengelegt.

## Festgelegte Auslegung

- Der Regeltext nennt „Bavaria Auto-Werke“ nicht in der Liste der acht Aktien. Für den Kaufvergleich in Regel 3 werden deshalb Volkswagen-Käufe mit Telekom-Käufen verglichen.
- „Ruhrstahl Metall“ fehlt ebenfalls in der Aktienliste. Für Regel 7 wird stattdessen die Kursänderung von Verteidigungsstahl verwendet.

## Weitere Ideen

- Noch keine offenen Ideen dokumentiert.
