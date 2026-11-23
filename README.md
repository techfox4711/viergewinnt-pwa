# Vier gewinnt PRO

**Installierbares Vier-Gewinnt-Spiel für Smartphone und Desktop** – ein Mensch spielt gegen einen starken Computergegner. Die Anwendung ist als Progressive Web App (PWA) für Android, iPhone, iPad, Linux und Windows umgesetzt.

## Aktueller Stand

Die **Spieldateien sind im Repository vorhanden**. Das Spiel kann nach dem Öffnen von `index.html` direkt im Browser gespielt werden. Für den zuverlässigen PWA-/Offline-Betrieb ist eine Veröffentlichung über HTTPS (beispielsweise GitHub Pages) nötig.

**Wichtig:** Die Veröffentlichung über GitHub Pages ist damit noch **nicht automatisch aktiviert**. Die GitHub-Pages-Adresse darf erst als erreichbar gelten, wenn unter *Settings → Pages* eine erfolgreiche Bereitstellung angezeigt wird.

## Spielfunktionen

- Klassisches Raster mit **7 Spalten × 6 Reihen** und vollständigen Vier-gewinnt-Regeln
- **Mensch gegen Computer**, kein zweiter menschlicher Spieler erforderlich
- Computergegner mit Eröffnungsbuch sowie zeitbegrenzter Spielbaumsuche (iterative Vertiefung, Negamax, Alpha-Beta-Suche und Stellungstabelle)
- Einstellbare maximale Denkzeit: **2, 5, 10 oder 20 Sekunden**
- Animation der fallenden Spielsteine und deutliche Markierung der Gewinnlinie
- Sieg- und Rundenzähler, neue Runde und Rücksetzen des Punktestands
- Touchbedienung, sieben Spalten-Schaltflächen und Tastatureingaben
- Responsives Layout und separate KI-Berechnung im Web Worker, damit die Oberfläche bedienbar bleibt
- PWA-Manifest, App-Symbole und Service Worker zur Offline-Nutzung nach dem ersten erfolgreichen Laden

**Spielstärke:** Die KI versucht, sehr starke Züge zu finden; wegen der zeitbegrenzten Suche ist **nicht jeder Zug garantiert mathematisch optimal**.

## Projektdateien

```text
viergewinnt-pwa/
├── README.md
├── README_PWA.txt
├── VIER_GEWINNT_LIZENZEN.txt
├── index.html
├── manifest.webmanifest
├── sw.js
└── icons/
    ├── favicon-64.png
    ├── apple-touch-icon.png
    ├── icon-192.png
    └── icon-512.png
```

## Lokal ausprobieren

Zum Testen reicht ein lokaler HTTP-Server im Repositoryverzeichnis, z. B. mit Python:

```bash
python -m http.server 8000
```

Danach im Browser **http://localhost:8000/** öffnen. Alternativ ist die normale Spielseite ohne PWA-Funktionen häufig auch direkt über `index.html` startbar. Service Worker funktionieren beim direkten Öffnen über `file://` in der Regel nicht.

## GitHub Pages veröffentlichen

1. Auf GitHub das Repository öffnen und **Settings → Pages** wählen.
2. Unter **Build and deployment** als Quelle **Deploy from a branch** auswählen.
3. Branch **main** und Ordner **/(root)** einstellen, anschließend **Save**.
4. Auf die erfolgreiche Veröffentlichung warten und die von GitHub angezeigte URL öffnen.
5. Im Smartphone-Browser Spiel, Darstellung und Installation testen.

Voraussichtliche Adresse nach erfolgreicher Freischaltung: `https://techfox4711.github.io/viergewinnt-pwa/`. Sie ist **nicht als bereits aktiv bestätigt**.

## Auf Android und iPhone installieren

- **Android:** veröffentlichte HTTPS-Seite im unterstützten Browser öffnen, Menü → **App installieren** oder **Zum Startbildschirm hinzufügen**.
- **iPhone/iPad:** veröffentlichte Seite in Safari öffnen, **Teilen → Zum Home-Bildschirm** wählen.

Nach erfolgreichem ersten Laden und Zwischenspeichern kann die PWA auch offline genutzt werden. Browser- und Betriebssystemversionen können die Installationsschritte beeinflussen.

## Technische Prüfungen

Die JavaScript-Syntax wurde geprüft. Die KI wurde stichprobenartig mit Eröffnungs-, Gewinn- und Blockierstellungen getestet; dabei erkannte sie sofortige Gewinne sowie notwendige Blockaden korrekt. **Eine vollständige plattformübergreifende End-to-End-Prüfung steht noch aus**, insbesondere unter iOS und Android.

## Datenschutz, Hosting und Lizenz

Das Spiel benötigt kein Nutzerkonto und versendet nach dem vorliegenden Quellcode keine Spielzüge an einen eigenen Backend-Dienst. Beim Abruf einer über GitHub Pages gehosteten Seite gelten unabhängig davon die technischen Zugriffs- und Datenschutzbedingungen des Hosters.

Ein **öffentliches Repository** bedeutet, dass der Quellcode einsehbar ist. GitHub Pages bietet für diese Standardveröffentlichung keinen eingebauten Passwortschutz. Für den eigenen Spielcode wurde noch keine allgemeine Open-Source-Lizenz festgelegt. Hinweise zum im Paket referenzierten externen Eröffnungsbuch stehen in `VIER_GEWINNT_LIZENZEN.txt`; dessen Lizenzherkunft ist vor weiterer Weiterverbreitung abzugleichen.

---

Projekt: **techfox4711/viergewinnt-pwa**
