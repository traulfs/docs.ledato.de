# docs.ledato.de

Technische Dokumentation der [Ledato GmbH](https://ledato.de) (Berlin) zu LED-Panels, App-Steuerung und Montagelösungen für digitale Außenwerbung.

Aufgebaut mit [Material for MkDocs](https://squidfunk.github.io/mkdocs-material/), analog zu [docs.taskit.de](https://docs.taskit.de): zweisprachig (DE/EN) über `mkdocs-static-i18n`, Volltextsuche, optionale eingebettete API-Referenzen über `mkdocs-swagger-ui-tag`. Das Farbschema orientiert sich an [ledato.de](https://ledato.de) (Petrol/Türkis `#008ba3` als Akzentfarbe, Logo im LED-Punktraster-Stil).

## Lokal starten

```bash
python3 -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
mkdocs serve
```

Die Seite ist dann unter <http://127.0.0.1:8000> erreichbar.

## Struktur

```
docs/
├── assets/            Logo, Favicon
├── stylesheets/        extra.css (Markenfarben, Feinschliff)
├── de/                 deutsche Inhalte (Standardsprache)
│   ├── LED-Panels/
│   ├── App-Steuerung/
│   ├── Montage/
│   └── Anwendungen/
└── en/                 englische Inhalte (gleiche Struktur)
```

## Hinweise

- Die Inhalte unter `docs/de` und `docs/en` sind aktuell Platzhalter (siehe `!!! todo`-Hinweise) und sollten schrittweise mit echten Produktdaten gefüllt werden.
- `repo_url` in `mkdocs.yml` verweist auf `traulfs/docs.ledato.de` — bei Bedarf an das tatsächliche Repository anpassen.
- Deployment erfolgt automatisch über GitHub Pages (`.github/workflows/deploy.yml`) bei jedem Push auf `main`. Dafür muss im Repository unter Settings → Pages die Quelle auf "GitHub Actions" gestellt werden.
