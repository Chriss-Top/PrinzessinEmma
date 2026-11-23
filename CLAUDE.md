# Prinzessinnen-Tag – Hinweise für Claude Code

Kinderspiel (Zielgruppe: Grundschulalter), erfunden von Emma. Alle Texte im Spiel sind auf Deutsch, kurz und kindgerecht.

## Aufbau
- Alles steckt in **einer Datei**: `index.html` (HTML + CSS + JS, keine Abhängigkeiten, kein Build).
- Gerendert wird mit Canvas 2D; die logische Spielfläche ist `W=1000, H=650` und wird an den Bildschirm angepasst (`fitGarden`).
- Drei Bildschirme: `#start` → `#dress` (Ankleidezimmer) → `#garden` (Hofgarten). Umschalten mit `show(id)`.
- Zustand im Objekt `S` (Name, Tag, Sterne, Outfit, `grownToday`, `celebrated`), gespeichert über `save()` in localStorage (immer mit try/catch).

## Wichtige Teile in index.html
- `DRESSES`, `COLORS`, `HAIRS`, `HAIRCOLORS`, `ACCS`: Auswahl im Ankleidezimmer
- `drawPrincess(c,x,y,scale,outfit,t,walking)`: zeichnet die Prinzessin in Einheiten (Füße bei 0,0, ca. 62 Einheiten hoch). Wird für den Spiegel und für den Garten benutzt.
- `ANIMALS`: Tiere mit Heimatposition, Futter und Geräusch. `care(animal, 'futter'|'wasser'|'liebe')`
- `PLOTS`, `SEEDS`, `plant()`, `water()`, `pick()`: Beete. Stufen: 0 leer, 1 Samen, 2 Keimling, 3 blüht
- `findNear()` + `buildActions()`: die Aktionsknöpfe unten, je nachdem, was in der Nähe ist
- `checkPerfect()`: Ziel des Tages (5 Tiere glücklich + 3 Pflanzen gewachsen), danach `goSleep()` → neuer Tag
- `emoji()`: Emojis werden über einen Offscreen-Canvas-Cache gezeichnet (`emojiImg`). Nicht auf direktes `fillText` mit großer Schrift zurückbauen, weil Chrome sie dann teils durchsichtig rendert.

## Regeln
- Keine bekannten Figuren oder Marken (Disney usw.). Nur eigene Designs.
- Es muss auf Touch-Geräten funktionieren (große Knöpfe, Tippen zum Laufen).
- Nach Änderungen in einem Browser testen: Start → Ankleiden → Garten → perfekten Tag erreichen.
