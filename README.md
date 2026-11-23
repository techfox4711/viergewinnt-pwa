# Vier gewinnt PRO

Eine browserbasierte Version des klassischen **Vier gewinnt** als Progressive Web App (PWA) für Smartphones, Tablets und Desktop-Computer.

> **Projektstatus:** Das Repository befindet sich im Aufbau. Die Anwendung ist erst spielbar und installierbar, sobald die Programmdateien hochgeladen und GitHub Pages eingerichtet wurden.

## Spielkonzept

- **Ein Mensch spielt gegen den Computer.**
- Klassisches Spielfeld mit **7 Spalten und 6 Reihen**.
- Ziel: Vier eigene Spielsteine waagerecht, senkrecht oder diagonal verbinden.
- Benutzerfreundliche Oberfläche mit deutlicher Hervorhebung einer Gewinnreihe.
- Anpassung an Maus, Touchscreen sowie unterschiedliche Bildschirmgrößen.
- Geplant ist ein besonders starker Computergegner mit effizienter Spielbaumsuche.

## Geplante Funktionen

| Bereich | Ziel |
| --- | --- |
| Spielmodus | Mensch gegen Computer |
| Spielfeld | 7 Spalten × 6 Reihen (klassische Regeln) |
| Gegner | Starke KI, z. B. Minimax mit Alpha-Beta-Suche, Zugreihenfolge und Positionsbewertung |
| Grafik | Flüssige Darstellung und gut erkennbare Gewinnmarkierung |
| Plattformen | Browser auf Windows, Linux, Android und iOS |
| Installation | PWA zum Starten vom Homescreen |
| Offline-Modus | Nutzung ohne Internet nach erfolgreicher Installation und Zwischenspeicherung |

Die tatsächliche Umsetzung der genannten Funktionen wird bei der Integration des Spielcodes und in den Tests überprüft.

## Vorgesehene Projektstruktur

```text
viergewinnt-pwa/
├── README.md
├── index.html
├── manifest.webmanifest
├── sw.js
└── icons/
    ├── icon-192.png
    └── icon-512.png
```

Die Verzeichnisstruktur ist ein Zielzustand, **keine Bestätigung bereits vorhandener Dateien**. Ergänzende HTML-, CSS-, JavaScript- und Testdateien können bei Bedarf hinzukommen.

## Lokal starten

Nach dem Hochladen der Programmdateien kann `index.html` in einem Browser geöffnet werden. Für einen vollständigen Test der PWA, insbesondere des Service Workers, empfiehlt sich ein lokaler Entwicklungsserver oder eine HTTPS-Veröffentlichung. Der Offline-Modus funktioniert nicht zuverlässig beim direkten Öffnen über `file://`.

## Veröffentlichung über GitHub Pages

1. Alle notwendigen Anwendungsdateien in das Repository übertragen.
2. Auf GitHub **Settings → Pages** öffnen.
3. Unter **Build and deployment** die Veröffentlichung aus einem Branch auswählen.
4. **main** und **/(root)** auswählen und speichern.
5. Die von GitHub angezeigte Pages-Adresse öffnen und die Anwendung testen.

**Wichtig:** Ein veröffentlichtes GitHub-Pages-Spiel ist grundsätzlich öffentlich erreichbar. Ein privates Repository oder ein Passwort in JavaScript stellt keinen zuverlässigen Zugriffsschutz für die Webseite dar.

## Installation auf Mobilgeräten

Diese Schritte gelten **nach** erfolgreicher Veröffentlichung und Einrichtung des PWA-Manifests.

### Android

Die veröffentlichte Seite in einem kompatiblen Browser (z. B. Chrome) öffnen und im Browsermenü **App installieren** oder **Zum Startbildschirm hinzufügen** auswählen. Die genaue Bezeichnung hängt vom Browser ab.

### iPhone / iPad

Die veröffentlichte Seite in Safari öffnen, das Teilen-Menü aufrufen und **Zum Home-Bildschirm** wählen. Die Beschriftungen können je nach iOS-Version abweichen.

## Tests vor der Freigabe

- Vier Steine in einer waagerechten, senkrechten und diagonalen Linie erkennen.
- Volle Spalten und ein unentschiedenes Spiel korrekt behandeln.
- Mensch und Computer müssen abwechselnd genau einen gültigen Zug ausführen.
- Die vier Gewinnsteine sauber und eindeutig hervorheben.
- Touchbedienung und responsives Layout auf Android und iPhone überprüfen.
- PWA-Installation sowie den Offline-Betrieb nach dem ersten Online-Laden testen.
- Die Stärke und Antwortzeit der Computer-KI systematisch prüfen.

## Datenschutz und Sicherheit

Die endgültigen Datenschutzeigenschaften hängen von den tatsächlich eingebundenen Skripten, Ressourcen und Diensten ab. Ziel ist eine möglichst lokal ausführbare Anwendung **ohne Benutzerkonto und ohne Verarbeitung persönlicher Spieldaten auf einem eigenen Server**. Vor der Veröffentlichung müssen mögliche externe Abhängigkeiten und die Hosting-Dienste geprüft werden.

## Lizenz

In diesem Repository ist zunächst **keine Open-Source-Lizenz** hinterlegt. Die öffentliche Sichtbarkeit des Quellcodes bedeutet nicht, dass Dritte ihn beliebig weiterverwenden dürfen. Vor einer Freigabe unter einer bestimmten Lizenz ist eine ausdrückliche Entscheidung erforderlich.

---

**Repository:** [techfox4711/viergewinnt-pwa](https://github.com/techfox4711/viergewinnt-pwa)
