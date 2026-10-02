# Fehlerradar

Analysiert eigene Schachpartien: Wo war die Stellung schwer, wo hast du stark gespielt, wo unnötig danebengegriffen?
Partie als PGN oder FEN einfügen oder per chess.com- bzw. Lichess-Benutzername laden.

- **Schwierigkeit**: ein kleines neuronales Netz (64×4-ResNet, 0,31 Mio. Parameter), trainiert auf rund 60 Mio. Stellungen
  aus Lichess-Partien (Rapid und Classical). Es schätzt, wie wahrscheinlich ein Spieler mit gegebenem Rating in einer
  Stellung eine Ungenauigkeit, einen Fehler oder einen Patzer begeht.
- **Ergebnis**: Stockfish 19 lite bewertet jeden Zug im Browser (Tiefe 16). Ein Fehler ist wie bei Lichess ein Verlust
  von mindestens 20 Prozentpunkten Gewinnchance.

Alles läuft in deinem Browser, Partien werden nicht hochgeladen. Abrufe gehen nur an die APIs von chess.com und Lichess,
wenn du einen Benutzernamen eingibst.

## Aktualisieren

Diese Seite ist der Build `demo/fehlerradar2/dist/fehlerradar_lokal.html` aus dem (privaten) Projekt-Repo, kopiert als
`index.html`.

## Lizenz

GPLv3 (siehe `LICENSE`), weil die Seite Stockfish enthält.

- Stockfish 19 lite: GPLv3, Quellcode <https://github.com/official-stockfish/Stockfish>,
  WebAssembly-Fassung <https://github.com/nmrugg/stockfish.js>
- chess.js 0.10.3: BSD
- Schriften Bricolage Grotesque und Hanken Grotesk: SIL Open Font License
- Figuren: cburnett (aus python-chess)
- Beispielpartien: Lichess-Datenbank (CC0)
