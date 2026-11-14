# Ideen und Änderungen

Dieses Dokument hält die umgesetzten Spielentscheidungen und spätere Ideen fest. Neue Einträge werden chronologisch ergänzt.

## Umgesetzt am 14.11.2026

- Startkapital je Depot auf 20.000 € gesetzt; alle acht Startkurse auf 5.000 € und der Mindestkurs auf 200 € gesetzt.
- Die bisherigen Titel durch die acht deutschen Unternehmen aus dem Spielprinzip ersetzt.
- Prozentuale Kurs- und Vermögensanzeigen durch absolute Eurobeträge ersetzt.
- Die acht geheimen Kursregeln als geordnete Berechnung bei Rundenbeginn umgesetzt. Der zufällige Telekom-Geheimnisstatus wird auf der Host-Tafel durch 🔒 kenntlich gemacht; die Regeln selbst erscheinen nicht in der Spieloberfläche.
- Die Host-Tabelle durch ein 4×2-Kartenraster mit individuellem SVG-Kursverlauf und Klassen-Handelszahlen ersetzt.
- Host-Steuerungen zum Pausieren/Fortsetzen und vorzeitigen Beenden ergänzt; Clients können während der Pause nicht handeln.
- Die PeerJS-Kommunikation zwischen Host und Clients beibehalten.
- Im Repository existiert keine `index.html`; die bestehende Anwendung liegt in `boersen-spiel.html`, die deshalb angepasst wurde.

## Festgelegte Auslegung

- Der Regeltext nennt „Bavaria Auto-Werke“ nicht in der Liste der acht Aktien. Für den Kaufvergleich in Regel 3 werden deshalb Volkswagen-Käufe mit Telekom-Käufen verglichen.
- „Ruhrstahl Metall“ fehlt ebenfalls in der Aktienliste. Für Regel 7 wird stattdessen die Kursänderung von Verteidigungsstahl verwendet.

## Weitere Ideen

- Noch keine offenen Ideen dokumentiert.
