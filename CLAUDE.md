# Prinzessinnen-Tag – Hinweise für Claude Code

Kinderspiel (Zielgruppe: Grundschulalter), erfunden von Emma. Alle Texte im Spiel sind auf Deutsch, kurz und kindgerecht.

## Aufbau
- Alles steckt in **einer Datei**: `index.html` (HTML + CSS + JS, keine Abhängigkeiten, kein Build).
- Gerendert wird mit Canvas 2D; die logische Spielfläche ist `W=1000, H=650` und wird an den Bildschirm angepasst (`fitGarden`).
- Drei Bildschirme: `#start` → `#dress` (Ankleidezimmer) → `#garden` (Hofgarten). Umschalten mit `show(id)`.
- Zustand im Objekt `S` (`two`, `players[0..1]` mit `name` + `outfit`, Tag, Sterne, `grownToday`, `celebrated`), gespeichert über `save()` in localStorage (immer mit try/catch). Alte Spielstände mit `name`/`outfit` werden beim Laden nach `players[0]` übernommen.
- Namen immer über `esc()` / `pname(i)` in HTML einsetzen; `whoTxt()` liefert „Prinzessin A (und Prinzessin B)“.

## Wichtige Teile in index.html
- `DRESSES`, `COLORS`, `HAIRS`, `HAIRCOLORS`, `ACCS`: Auswahl im Ankleidezimmer
- `drawPrincess(c,x,y,scale,outfit,t,walking)`: zeichnet die Prinzessin in Einheiten (Füße bei 0,0, ca. 62 Einheiten hoch). Wird für den Spiegel und für den Garten benutzt.
- `ANIMALS`: Tiere mit Heimatposition, Futter und Geräusch. `care(animal, 'futter'|'wasser'|'liebe')`
- `PLOTS`, `SEEDS`, `plant()`, `water()`, `pick()`: Beete. Stufen: 0 leer, 1 Samen, 2 Keimling, 3 blüht
- `PL[0..1]`: die Prinzessinnen im Garten (Position, Ziel, `near`, Steuerknüppel `jx/jy`). `NP()` = Anzahl aktiver Spielerinnen. `movePlayer()` bewegt eine Prinzessin (Tippen, Tasten, Steuerknüppel) und läuft um Brunnen/Teich herum.
- `findNear(P)` + `buildActions(i)`: die Aktionsknöpfe je Spielerin (`#actions0`, `#actions1`), je nachdem, was in der Nähe ist
- Zwei-Spieler-Modus (`S.two`): `#stage.duo` reserviert unten eine Steuerleiste (`--bar`), `fitGarden()` lässt dafür Platz. Steuerknüppel `#stick0/1`; Tippen auf den Garten ist zu zweit aus. Tasten: WASD = Spielerin 1, Pfeile = Spielerin 2.
- `checkPerfect()`: Ziel des Tages (5 Tiere glücklich + 3 Pflanzen gewachsen), danach `goSleep()` → neuer Tag
- `emoji()`: Emojis werden über einen Offscreen-Canvas-Cache gezeichnet (`emojiImg`). Nicht auf direktes `fillText` mit großer Schrift zurückbauen, weil Chrome sie dann teils durchsichtig rendert.

## Regeln
- Keine bekannten Figuren oder Marken (Disney usw.). Nur eigene Designs.
- Es muss auf Touch-Geräten funktionieren (große Knöpfe, Tippen zum Laufen).
- Nach Änderungen in einem Browser testen: Start → Ankleiden → Garten → perfekten Tag erreichen, und zwar mit einer **und** mit zwei Prinzessinnen.
