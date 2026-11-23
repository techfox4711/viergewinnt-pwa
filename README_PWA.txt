VIER GEWINNT PRO – Progressive Web App (PWA)
===========================================

Startseite: index.html
Manifest: manifest.webmanifest
Offline-Cache: sw.js
App-Symbole: icons/

GitHub Pages aktivieren:
Repository → Settings → Pages → Deploy from a branch → main → /(root).
Nach Veröffentlichung URL auf Smartphone öffnen.
Android: Browsermenü → App installieren / Zum Startbildschirm hinzufügen.
iPhone: Safari → Teilen → Zum Home-Bildschirm.

Zum lokalen Test:
python -m http.server 8000
Browser: http://localhost:8000/

Wichtig:
Ohne GitHub-Pages-Veröffentlichung ist die App nicht über eine öffentliche URL
erreichbar. Eine veröffentlichte GitHub-Pages-Seite ist grundsätzlich öffentlich.
Eine installierte PWA kann nach dem ersten erfolgreichen Online-Laden offline
verwendet werden, sofern der Cache vollständig eingerichtet wurde.
