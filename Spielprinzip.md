# Spielprinzip

## Ziel

Die Börsen-Arena ist eine Börsensimulation für eine Klasse. Die Lehrkraft eröffnet als Host einen Raum und zeigt die gemeinsame Börsentafel. Die Schüler treten mit einem Raum-Code als Clients bei und verwalten jeweils ihr eigenes Depot. Am Ende gewinnt das Team mit dem höchsten Gesamtvermögen.

## Start und Handel

- Jedes Depot startet mit **20.000 € Bargeld**.
- Es gibt acht Aktien. Ihr Startkurs beträgt jeweils **5.000 €**; kein Kurs kann unter **200 €** fallen.
- Während einer Runde können die Schüler Aktien kaufen und verkaufen. Der Client zeigt Bargeld, Depotwert, Gesamtvermögen sowie den Gewinn oder Verlust in Euro.
- Eine Partie umfasst 24 Runden. Standardmäßig dauert eine Runde fünf Minuten; der Host kann vor Spielbeginn den kurzen Testmodus wählen.
- Der Host kann die Partie anhalten und fortsetzen oder vorzeitig beenden. Während einer Pause stehen auch Käufe und Verkäufe still.
- Nach Spielende und bei Verbindungsverlust können Clients über „Nochmal spielen“ zur Startansicht zurückkehren. Auch die Host-Siegerehrung bietet diesen Neustart an.
- Die Verbindung zwischen Host und Clients läuft über PeerJS. Der Host verwaltet die gemeinsame Tafel und sendet Kurs- und Rundendaten an die verbundenen Clients.

## Aktien

1. Verteidigungsstahl
2. Alt-Entertaiment
3. Volkswagen Auto-Werke
4. Telekom & Tech Süd
5. Cyber Securit
6. Nordwind Energie
7. Hochtief Bauwesen
8. Rhein-Main Bank AG

## Kurswechsel

Die Kursänderungen werden bei Rundenbeginn in der folgenden Reihenfolge berechnet. Diese Regeln sind absichtlich nicht Teil der Bildschirmoberfläche. Kursänderungen sind feste Euro-Beträge; alle Kurse bleiben mindestens 200 €.

1. **Verteidigungsstahl:** Der Gesamtbestand der Klasse wird mit dem Bestand der Vorrunde verglichen. Je Anteil Zunahme sinkt der Kurs um 200 €, je Anteil Abnahme steigt er um 200 €.
2. **Alt-Entertaiment:** In ungeraden Runden steigt der Kurs um 700 €, in geraden Runden sinkt er um 500 €.
3. **Volkswagen Auto-Werke:** Wurden in der Vorrunde mehr Volkswagen- als Telekom-Anteile gekauft, steigt der Kurs um 1.200 €. Andernfalls sinkt er um 600 €.
4. **Telekom & Tech Süd:** Bei einem Klassenbestand von 10 bis einschließlich 30 Anteilen steigt der Kurs um 1.300 €, sonst sinkt er um 800 €. Zu Beginn jeder Runde wird unabhängig davon mit 40 % Wahrscheinlichkeit ein Geheimnisstatus aktiviert, der auf der Host-Tafel mit 🔒 markiert wird.
5. **Cyber Securit:** Bei aktivem Geheimnisstatus der Telekom-Aktie steigt der Kurs um 900 €, sonst sinkt er um 700 €.
6. **Nordwind Energie:** Wurden in der Vorrunde über alle Aktien hinweg mehr als 15 Anteile gekauft, steigt der Kurs um 700 €, sonst sinkt er um 400 €.
7. **Hochtief Bauwesen:** Ist der Kurs von Verteidigungsstahl in diesem Rundenwechsel gestiegen, steigt Hochtief um 600 €, sonst sinkt der Kurs um 600 €.
8. **Rhein-Main Bank AG:** Sind mindestens vier der sieben anderen Aktien gestiegen, steigt der Kurs um 800 €. Sind mindestens vier gefallen, sinkt er um 500 €. Andernfalls bleibt er unverändert.

Die im Regeltext erwähnten Vergleichswerte „Bavaria Auto-Werke“ und „Ruhrstahl Metall“ sind in der Aktienliste nicht enthalten. Für die Umsetzung vergleicht Regel 3 deshalb Volkswagen-Käufe mit Telekom-Käufen; Regel 7 verwendet den Kurs von Verteidigungsstahl.

## Tafel und Spielende

Die Host-Tafel zeigt alle acht Aktien in einem 4×2-Kartenraster mit Kurs, absoluter Änderung in Euro, Kursverlauf sowie Käufen, Verkäufen und Gesamtbesitz der Klasse. Nach Runde 24 werden die Endvermögen der Clients an den Host übermittelt und als Rangliste angezeigt.
