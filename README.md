# myrror

**Ein Android-Handy, zwei Bildschirme.** myrror macht die Sitzung von Handy A
auf Handy B nutzbar, während Handy A belegt ist, etwa weil Claude darauf Apps
automatisiert testet.

## Stand

Evaluation abgeschlossen, Umsetzung noch nicht begonnen. Ergebnis und
Empfehlung: [docs/evaluation-android.md](docs/evaluation-android.md).

## Prinzip

Zwei Geräte lassen sich nicht in Echtzeit vollständig *replizieren*. Möglich
ist aber eine **Projektion**: Handy A bekommt ein zweites, virtuelles Display.
Dieses Display wird auf Handy B gestreamt und von dort bedient. Claude testet
parallel auf dem physischen Display von Handy A. Dienste, die sich nicht
streamen lassen (Banking, Mikrofon, Telefonie, NFC), laufen über
Multi-Device-Apps und MultiSIM direkt auf Handy B.

## Geplanter Aufbau

| Pfad | Inhalt |
|---|---|
| `docs/` | Evaluation, Architekturentscheidungen, Setup-Anleitungen |
| `host/` | PC-Seite: Pairing- und Diagnose-Skripte, Display-Guard für Claudes Testwerkzeuge |
| `client-android/` | Client-App für Handy B |
| `CLAUDE.md` | Regeln für Gerätetests durch Claude |
