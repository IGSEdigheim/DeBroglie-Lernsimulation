# De-Broglie-Simulation – Spezifikation

**Umsetzung:** `index.html` im selben Ordner (zweite Fassung 05.11.2026). Das Lernpaket `DeBroglie_SCORM.zip` (SCORM 1.2) enthält diesen Stand, in Moodle ist es noch nicht.
Direkt zu einem Schritt springen: `index.html#schritt=7`.

**Lehrermodus:** Beim Öffnen jedes Schritts sind die zu berechnenden Werte ausgefüllt (Selbstchecks und Tabelle; bei zu wenigen Zeilen kommen 3, 5 und 7 kV dazu, in Schritt 7 auch die Radien), und im Anleitungsfeld stehen die genauen Werte.
- **Strg + Umschalt + L** schaltet ihn jederzeit an und aus, auch in Moodle. In dieser Zeit wird nichts gespeichert (auch kein „abgeschlossen“), beim Ausschalten kommt der vorherige Stand zurück.
- **Dauerhaft:** In `index.html`, Zeile 6, `false` durch `true` ersetzen, speichern, Seite neu laden. Die Testwerte werden getrennt vom normalen Stand gespeichert. **Vor dem Bau des Lernpakets muss dort wieder `false` stehen.**

**Lizenz:** MIT, `LICENSE` im selben Ordner (Copyright 2026 Pascal Deneaux), der Text steht auch unten in `index.html`. Auf der Seite steht er kurz in der Fußzeile.

**Formeln:** KaTeX 0.16.11 (MIT-Lizenz, Lizenztext in der Datei) ist samt Schriften in `index.html` eingebettet, die Datei läuft also offline. Formeln stehen im Quelltext als LaTeX: `\( … \)` im Fließtext, `\[ … \]` als eigene Zeile. Eingebettet sind nur die Schriften Main, Math und Size; Sonderalphabete wie `\mathbb` fehlen.

Stand: 05.11.2026 · Vom Fotoeffekt ist nur das Design übernommen (und das Speichern in Moodle), nicht der Aufbau des Lernprogramms. Das AB De Broglie spielt für die Simulation keine Rolle.

## Grundgedanke
**Erst der Versuch, dann die Rechnung.** Die Schüler beginnen und enden am selben Schirm. Jeder Schritt beantwortet die Frage, die der vorige aufwirft.

| Schritt | Leitfrage | Was die Schüler tun | Prüfung |
|---|---|---|---|
| 1 Beobachten | Was passiert auf dem Schirm? | Heizung an, Folie raus und rein, Spannung ändern, Vermutung notieren | Auswahlfrage |
| 2 Idee | Können Elektronen eine Wellenlänge haben? | *p* = *h*/*λ* für das Photon herleiten, *λ* = *h*/*p* kennenlernen | Auswahlfrage |
| 3 Impuls | Wie groß ist der Impuls? | *p* und die klassische Formel herleiten | *v* bei eingestellter Spannung |
| 4 Vorhersage | Wie groß ist die Wellenlänge? | Mindestens 3 Spannungen wählen, *λ* berechnen | Tabelle prüft |
| 5 Bragg | Warum nur bestimmte Winkel? | Δ*s* begründen, *θ*-Regler | *θ* für *n* = 1 |
| 6 Formel | Wie kommt man vom Ring zu *λ*? | Formel herleiten | *λ* für *r* = 15 mm |
| 7 Messen | Hatte de Broglie recht? | Inneren Ring messen, *λ* berechnen, vergleichen, Vermutung prüfen | Tabelle prüft |
| 8 Ringe (Zusatz) | Warum Ringe? | Kristallite | – |
| 9 Ausblick (Zusatz) | – | Zeitleiste, Elektronenmikroskop, Alltagsobjekte | – |

Ein Auftrag pro Hauptschritt, 5 Selbstcheck-Fragen. Skizzen und Abzeichnen sagt der Lehrer im Unterricht an, sie stehen nicht in der Simulation. Der Text bleibt ausführlich.

## Bedienung
- **Zwei feste Felder:** links die Spannung, daneben immer das Werkzeug des Schritts. Nichts taucht in einem leeren Bereich auf.
- **Layout:** Alle Kästen haben dieselbe feine Kante, auch das Simulationsfeld. Ab 1081 px Fensterbreite füllt die Szene die Höhe, die linke und die rechte Spalte schließen oben und unten bündig ab, und die Fußzeile ist immer sichtbar. Bei schmaleren Fenstern steht sie am Seitenende. Die Tabelle steht unter den Feldern, ein Hinweis in den Feldern der Schritte 4 und 7 weist darauf hin.
- **Heizung und Folie** sitzen in Schritt 1 im Feld „Röhre“, der Text nennt sie beim Namen. Ab Schritt 2 bleibt die Heizung an und die Folie im Strahl.
- **Spannung frei wählbar:** 1–10 kV, ±0,1 kV, Zahleneingabe.
- **Vergrößerungen:** Kanone, Welle, Folie und Dreieck zeigen in einer kleinen Röhre, wo man gerade ist.
- **Eine durchgehende Tabelle:** Zeile je Spannung mit *U*<sub>B</sub>, *λ* nach de Broglie (Schritt 4), dazu in Schritt 7 *r*, *λ* aus *r* und Abweichung. Eingaben werden mit 2 % Toleranz geprüft.
- **Messkreis:** auf dem Schirm ziehen, Regler, ±0,5 mm, Zahleneingabe. Er speichert nur Werte auf dem inneren Ring (Toleranz ±2 mm), sonst kommt ein Hinweis.

## Physikmodell
- *λ* = *h* / √(2 · *m*<sub>e</sub> · e · *U*<sub>B</sub>), klassisch.
- Röhre (Leybold 555 626): *L* = 135 mm, *d* = 213 pm, *n* = 1. Formelzeichen: *U*<sub>B</sub>, *E*<sub>el</sub>, *E*<sub>kin</sub>, *v*, *p*, *λ*, *m*<sub>e</sub>, *r*, *L*, *θ*, 2*θ*, *d*, *n*.
- *r* = *L* · tan(2 · arcsin(*λ* / (2*d*))). Festes *L* ohne Wölbung des Schirms („einfache Variante ohne Pythagoras“).
- **Nur der innere Ring wird behandelt.** Der äußere (intern mit *d* = 123 pm berechnet) bleibt sichtbar, aber zwei Netzebenenscharen kommen im Text der Hauptschritte nicht vor.
- Schritt 4: ein Bild, wirklich im selben Maßstab: quadratisches Gitter mit dem Abstand *d* in beiden Richtungen und die Welle (Atome kleiner gezeichnet). Die sechseckige Wirklichkeit zeigt der Zusatz „Ringe“.
- Bragg-Szene: quadratisches Gitter, feste Wellenlänge 100 pm nur zum Anschauen, *d* = 213 pm, nur *θ* regelbar (*n* = 1 bei 13,6°, *n* = 2 bei 28,0°, Auslöschung bei 6,7°).
  - Umschalter im Feld „Darstellung“: **Wie im Versuch** (Start: Strahl von links, Kristall um *θ* geneigt, Ablenkung 2*θ* eingezeichnet) und **Zum Abzeichnen** (Netzebenen waagerecht). Beides ist dieselbe Geometrie, nur gedreht.
  - Feine gestrichelte Linien (Wellenfronten) stehen senkrecht auf beiden Wellen und laufen mit einem Berg der oberen Welle mit. Die Punkte auf den Linien zeigen die Auslenkung beider Wellen: beim Einfall immer Berg und Berg, beim Austritt nur bei erfüllter Bragg-Bedingung.
- Rechte Winkel als Viertelkreis mit Punkt.
- Schreibweise: Formeln mit KaTeX, auch einzelne Symbole im Text und in den Bedienfeldern; die Beschriftungen in der Szene nutzen dieselben Schriften. Brüche immer mit waagerechtem Bruchstrich (kein Schrägstrich, kein „½“), Wurzeln mit Strich über dem ganzen Term, ohne Klammern. Nur Einheiten wie m/s und km/h bleiben mit Schrägstrich.

| *U*<sub>B</sub> | *λ* | *r* innen | *r* außen |
|---|---|---|---|
| 1 kV | 38,8 pm | 24,9 mm | 44,2 mm |
| 3 kV | 22,4 pm | 14,3 mm | 24,9 mm |
| 5 kV | 17,3 pm | 11,0 mm | 19,2 mm |
| 7 kV | 14,7 pm | 9,3 mm | 16,2 mm |
| 10 kV | 12,3 pm | 7,8 mm | 13,5 mm |

## Schirmbild
Nach dem Foto einer echten Röhre bei 6,5 kV. Es diente nur als Maßstab, ist nicht eingebaut und liegt nicht mehr im Ordner. Radial gemittelter Grünwert des Fotos:

| | Foto bei 6,5 kV | in der Simulation |
|---|---|---|
| Hof um die Mitte | 154 · e^(−*ρ*/19,9 mm) + 232 · e^(−*ρ*/4,2 mm) | ebenso |
| Innerer Ring | bei 59 px, +23 auf Untergrund 125, Halbwertsbreite ca. 2 mm | ebenso |
| Äußerer Ring | bei 104 px, +18 auf Untergrund 71, Halbwertsbreite ca. 2,8 mm | ebenso |
| Radienverhältnis | 1,76 | 1,74 |

Bei 6,5 kV weicht die Simulation in den geprüften Radien um höchstens 8 von 255 vom Foto ab.

**Annahmen (dazu gibt es nur dieses eine Foto):** Der Hof schrumpft mit der Spannung wie die Ringe (Faktor √(6,5 kV / *U*<sub>B</sub>)), und der Schirm wird mit der Spannung heller (Faktor √(*U*<sub>B</sub> / 6,5 kV)).

## Korrekturen (06.11.2026)
Aus dem Test der Fotoeffekt-Simulation übernommen, Wortlaut und Physik unverändert:
- **Moodle:** Eigener Browserspeicher je Schüler, beim Öffnen gilt der neuere Stand, beim Schließen wird gesichert. Wird der Stand zu groß für Moodle, sagt eine Meldung das.
- **Selbstcheck:** Getippte, ungeprüfte Zahlen bleiben, wenn eine andere Frage beantwortet wird. Die Rückmeldung gilt immer für die letzte Antwort, ein erreichter Haken bleibt.
- **Schmale Fenster:** Feintaster und „Zum Abzeichnen“ ragen um 1100 px nicht mehr aus ihrem Feld.

## Für die nächste Überarbeitung
- Hinweis zur Spannungsgrenze prüfen: Leybold nennt 5 kV, die Stationsanleitung 6 kV, das Foto zeigt 6,5 kV. Im Text steht „etwa 5 bis 6 kV“.
- Lernpaket abgenommen und ersetzt am 06.11.2026 (Kurs 330, cmid 36908). Nach weiteren Änderungen erst nach der Abnahme mit `paket.py` bauen und mit `moodle replace-file 36908 DeBroglie_SCORM.zip` ersetzen.

## Quellen
- Röhrendaten: [Leybold 555 626](https://www.leybold-shop.com/en/555626), [Versuchsanleitung P6.1.5.1](https://sammlung.physik.rwth-aachen.de/Versuche/Quantenphysik/Elektronenbeugung/Anleitungen/Leybold/Elektronenbeugung_p6151_d.pdf)
- Zeitleiste: [Nobelpreis 1929](https://www.nobelprize.org/prizes/physics/1929/summary/), [Nobelpreis 1986](https://www.nobelprize.org/prizes/physics/1986/summary/), [Ruska (Autobiografie)](https://www.nobelprize.org/prizes/physics/1986/ruska/auto-biography/), [Davisson (Britannica)](https://www.britannica.com/biography/Clinton-Davisson), [Doppelspaltversuch](https://en.wikipedia.org/wiki/Double-slit_experiment) (Jönsson 1961), [Physics World](https:/a.org/wiki/Double-slit_experiment) (Jönsson 1961), [Physics World](https://physicsworld.com/?p=23202) (C60, Arndt et al. 1999)
