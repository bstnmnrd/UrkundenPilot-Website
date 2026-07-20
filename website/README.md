# UrkundenPilot-Landingpage

Diese statische Website ist für die geschlossene Pilotphase vorgesehen. Sie enthält
keinen öffentlichen Download, keine Nutzungsanalyse, keine externen Schriftarten und
keine eingebetteten Drittinhalte.

## Lokale Vorschau

Vom Projektordner aus:

```text
rm -rf /tmp/urkundenpilot-site
mkdir -p /tmp/urkundenpilot-site/assets
cp website/*.html website/robots.txt /tmp/urkundenpilot-site/
cp website/assets/site.css assets/UrkundenPilot-logo.png /tmp/urkundenpilot-site/assets/
python3 -m http.server 8765 --directory /tmp/urkundenpilot-site
```

Danach `http://localhost:8765` öffnen.

## Veröffentlichung über GitHub Pages

Der Workflow `.github/workflows/pages.yml` veröffentlicht ausschließlich die Dateien
aus `website` sowie das vorhandene UrkundenPilot-Logo. Programmpakete, Quellcode und
interne Dokumentation werden nicht Teil des Website-Artefakts.

Da das eigentliche UrkundenPilot-Repository privat bleibt, wird die Website in das
separate öffentliche Repository `bstnmnrd/UrkundenPilot-Website` übernommen. Nur in
diesem Repository führt der Workflow die Veröffentlichung aus. Änderungen werden
zuerst hier als kanonische Quelle gepflegt, geprüft und anschließend in das reine
Website-Repository übernommen.

Im GitHub-Repository einmalig unter `Settings → Pages` als Quelle `GitHub Actions`
auswählen. Nach einem Push auf `main` wird die Seite automatisch aktualisiert.

Die öffentliche Hauptadresse lautet:

```text
https://urkundenpilot.de/
```

Die technische GitHub-Pages-Adresse bleibt im Hintergrund bestehen und wird auf die
eigene Domain weitergeleitet.

Vor einer öffentlichen kommerziellen Nutzung sind Impressum und Datenschutzerklärung
rechtlich zu prüfen. GitHub Pages ist für eine Projekt- und Pilotseite geeignet, aber
nicht als dauerhafte Plattform für einen Online-Shop oder primär kommerzielle
Transaktionen vorgesehen.
