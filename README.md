# gameday-tv

Senderliste für die private GameDay-App (https://gameday-6u3.pages.dev).
Die App liest `tv.json` alle 30 Minuten und markiert passende Spiele als „Session bestätigt“.

## Eintrag-Format
```json
{ "date": "2026-11-23", "comp": "nfl", "match": ["49ers", "vikings"], "name": "RTL",
  "additional": "Sky Sport · RTL+", "note": "kurze Begründung", "source": "https://…" }
```
- `date`: Spieltag in **deutscher Zeit** (Nachtspiele zählen zum Folgetag, z. B. 02:20 Uhr am Montag → Montag)
- `comp`: `ger.1`, `ger.2`, `ger.dfb_pokal`, `uefa.champions`, `uefa.europa`, `uefa.europa.conf`, `nfl`, `nba`, `f1` …
- `match`: Wörter, die alle im Spieltitel stehen müssen (ESPN-Namen, englisch, z. B. "Bayern Munich")
- `session` (nur F1): z. B. "Rennen", "Qualifying"
- Nur offiziell bestätigte Angaben eintragen (Sender-Pressemitteilungen, bundesliga.com TV-Plan, DFB, Sky/RTL-Programm).
