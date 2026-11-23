# 👑 Prinzessinnen-Tag

Ein kleines Browserspiel für Kinder im Grundschulalter. Die Idee stammt von Emma.

Du bist eine Prinzessin. Morgens suchst du dir im Schloss Kleid, Frisur und Schmuck aus. Danach geht es in den Hofgarten. Dort versorgst du die Tiere und pflanzt Blumen.

**Ziel:** Hab den perfekten Tag! Alle 5 Tiere sollen glücklich sein und 3 Pflanzen blühen. Dann gehst du schlafen und ein neuer Tag beginnt.

## Spielen

- **Online:** https://chriss-top.github.io/PrinzessinEmma/ (wenn GitHub Pages eingeschaltet ist, siehe unten)
- **Ohne Internet:** `index.html` herunterladen und im Browser öffnen. Du brauchst keine Installation und keinen Server.

Das Spiel läuft am Computer, auf dem Tablet und auf dem Handy. Zu zweit macht es am meisten Spaß auf einem Tablet oder Computer.

## So geht's

1. **Eine oder zwei Prinzessinnen?** Wähle, ob du allein spielst oder zu zweit. Gib die Namen ein und tippe auf „Los geht's!“.
2. **Im Ankleidezimmer** Kleid, Farbe, Frisur, Haarfarbe und Schmuck aussuchen. Der Spiegel zeigt dir sofort, wie es aussieht. „Überrasch mich!“ wählt alles zufällig.
3. **Im Hofgarten** herumlaufen:
   - **Laufen:** Tippe oder klicke irgendwohin. Am Computer gehen auch die Pfeiltasten oder WASD.
   - **Etwas tun:** Geh nah an ein Tier, ein Beet, den Brunnen oder die Schlosstür. Unten erscheinen dann große Knöpfe.
   - Tippst du direkt auf ein Tier, läuft die Prinzessin zu ihm hin.

## 👸👸 Zu zweit spielen

Zwei Kinder spielen gemeinsam an einem Gerät. Jede steuert ihre eigene Prinzessin.

- **Ankleidezimmer:** Zwei Spiegel stehen nebeneinander. Oben tippst du an, wer sich gerade anzieht (oder du tippst direkt auf den Spiegel).
- **Im Garten** hat jede ihre eigene Ecke in der Leiste unten:
  - **Spielerin 1 (rosa)** links: Steuerknüppel und eigene Knöpfe
  - **Spielerin 2 (lila)** rechts: Steuerknüppel und eigene Knöpfe
  - Den Steuerknüppel mit dem Finger in die Richtung ziehen, in die die Prinzessin laufen soll. Beide können gleichzeitig laufen.
- **Am Computer:** Spielerin 1 läuft mit **W A S D**, Spielerin 2 mit den **Pfeiltasten**. Die Knöpfe werden mit der Maus geklickt.
- Über jeder Prinzessin steht ihr Name. Ein farbiger Ring zeigt, wo sie gerade etwas tun kann.
- **Ihr seid ein Team:** Die Sterne und das Ziel des Tages gehören euch beiden. Teilt euch die Arbeit auf, zum Beispiel: Eine kümmert sich um die Tiere, die andere um den Garten.

## Was es gibt

### 👗 Ankleidezimmer
| Kleid | So sieht es aus |
|---|---|
| Ballkleid | lang und weit wie eine Glocke, mit Puffärmeln und Rüschen |
| Sternenkleid | lang und schmal, mit Glitzer-Umhang und langen Ärmeln |
| Blumenkleid | kurzes Stufenkleid mit Blütensaum, man sieht die Schuhe |
| Herzchenkleid | kurzes Tutu wie bei einer Ballerina, mit Trägern |

Dazu kommen 7 Kleiderfarben, 5 Frisuren, 6 Haarfarben und Schmuck (Krone, Diadem, Blumenkranz, Schleife).

### 🐾 Tiere
Sternchen 🦄, Mimi 🐱, Hoppel 🐰, Quaki 🦆 und Bello 🐶. Jedes Tier will **Futter**, **Wasser** und **Streicheln**. Hat ein Tier alle drei Sachen bekommen, ist es überglücklich 💖.

### 🌱 Garten
6 Beete für Tulpe, Sonnenblume, Rose und Erdbeere. Samen pflanzen, gießen, warten und noch einmal gießen, dann blüht die Pflanze. Blühende Blumen kannst du bewundern oder pflücken.

### ✨ Außerdem
- Am **Wunschbrunnen** eine Münze werfen und dir etwas wünschen
- **Sterne** sammeln, bei jeder guten Tat gibt es welche
- Eine **Feier mit Konfetti** am Ende des perfekten Tages
- Über die **Schlosstür** zurück ins Ankleidezimmer
- Namen, Outfits, Spielmodus, Tag und Sterne merkt sich der Browser (localStorage)
- Ton an und aus mit 🔊 oben rechts

## GitHub Pages einschalten

Damit das Spiel unter dem Link oben erreichbar ist:

1. Im Repository auf **Settings → Pages** gehen.
2. Bei **Source** „Deploy from a branch“ wählen.
3. Branch `main` und Ordner `/ (root)` wählen und auf **Save** drücken.

Nach 1–2 Minuten ist das Spiel online. Jede Änderung auf `main` wird automatisch übernommen.

## Für Entwickler

- Alles steckt in **einer Datei**: `index.html` (HTML, CSS und JavaScript, ohne Abhängigkeiten und ohne Build-Schritt).
- Gezeichnet wird mit Canvas 2D. Die Figuren und Tiere sind eigene Designs.
- Mehr Hinweise zum Aufbau stehen in [`CLAUDE.md`](CLAUDE.md).
