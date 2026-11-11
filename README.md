# Schiffe versenken

Schiffe versenken für zwei Personen im selben Netzwerk – eine einzelne HTML-Datei, ohne Installation, ohne Server, ohne Admin-Rechte.

## Spielen

1. `schiffe-versenken.html` auf beide Rechner kopieren und per Doppelklick in Edge oder Chrome öffnen.
2. Eine Person klickt **Spiel eröffnen** und schickt den Einladungscode (z. B. per Teams).
3. Die andere klickt **Beitreten**, fügt den Code ein und schickt den Antwortcode zurück.
4. Antwortcode einfügen, Flotte aufstellen, **Bereit**.

Ohne Mitspieler gibt es einen Computergegner (Leicht/Schwer).

## Datenschutz

- Direkte, verschlüsselte WebRTC-Verbindung zwischen den beiden Browsern. Kein Vermittlungsserver, kein STUN/TURN.
- Eine Content-Security-Policy im Dateikopf verbietet jeden Abruf aus dem Internet.
- Übertragen werden nur Name, Schüsse, Treffermeldungen und Chat – nur an das Gegenüber.
- Im Browser gespeichert: Name, Ton- und Schwierigkeits-Einstellung.

## Fair Play

Vor Spielbeginn sendet jede Seite einen SHA-256-Fingerabdruck ihrer Aufstellung (mit Zufallssalz). Am Ende wird die Aufstellung aufgedeckt und gegen alle gegebenen Antworten geprüft.

## Regeln

10×10, fünf Schiffe (5, 4, 3, 3, 2), Schiffe berühren sich nicht. Wer trifft, schießt nochmal. Versenkte Schiffe legen ihr Umfeld automatisch als Wasser frei.

## Verbindung klappt nicht?

Browser verbergen die eigene IP hinter einem `.local`-Namen, den manche Firmennetze nicht auflösen. Dann im Verbindungsdialog **Direkte Netzwerkadresse verwenden** wählen (kurze Mikrofon-Freigabe, wird sofort wieder geschlossen) und den Code neu erzeugen. Gast-WLAN mit Client-Isolation verhindert direkte Verbindungen grundsätzlich.
