# ByteSuite Plugin Store

Der offizielle Plugin Store für ByteSuite. Hier findest du alle verfügbaren Plugins, um deine Anwendung zu erweitern.

## Verzeichnisstruktur

```
apps/store/
├── catalog.json              # Zentrale Plugin-Katalog-Datei (alle Plugins auf einen Blick)
├── schema.json               # Manifest-Schema-Definition für Plugin-Metadaten
├── README.md                 # Diese Datei
├── categories/
│   └── index.json            # Verfügbare Kategorien mit Beschreibungen
└── plugins/
    ├── inateck/
    │   └── manifest.json     # Detailliertes Manifest für Inateck Scanner
    └── uni-elektro/
        └── manifest.json     # Detailliertes Manifest für Uni-Elektro Import
```

## Plugin hinzufügen

Um ein neues Plugin zum Store hinzuzufügen:

1. **Ordner erstellen**: Erstelle einen neuen Ordner unter `plugins/<plugin-id>/`
2. **Manifest erstellen**: Füge eine `manifest.json` nach dem Schema in `schema.json` hinzu
3. **Katalog aktualisieren**: Trage das Plugin in `catalog.json` unter `plugins` ein
4. **Kategorie zuweisen**: Weise eine bestehende Kategorie aus `categories/index.json` zu oder erstelle eine neue

## Manifest-Schema

Jedes Plugin benötigt eine `manifest.json` mit folgenden Pflichtfeldern:

| Feld | Typ | Beschreibung |
|------|-----|-------------|
| `id` | string | Eindeutige ID (keine Leerzeichen, klein, Bindestriche erlaubt) |
| `name` | string | Anzeigename |
| `version` | string | SemVer (MAJOR.MINOR.PATCH) |
| `description` | string | Kurze Beschreibung (max. 200 Zeichen) |
| `type` | string | Plugin-Typ (scanner, product-import, reporting, etc.) |
| `category` | string | Kategorie-ID aus `categories/index.json` |
| `author` | string | Autor oder Organisation |
| `license` | string | Lizenz (MIT, Apache-2.0, GPL-3.0, proprietary) |
| `pricing` | string | Preismodell: `free`, `paid`, `freemium` |
| `downloadUrl` | string | Direkter Download-Link zur ZIP-Datei |
| `minAppVersion` | string | Minimale ByteSuite-Version |

## Kategorien

- **Hardware** – Scanner, Drucker, Peripheriegeräte
- **Integrationen** – Externe Dienste, Shops, Datenquellen
- **Berichte & Analysen** – Dashboards, Datenanalysen
- **Kommunikation** – E-Mail, SMS, Benachrichtigungen
- **Buchhaltung** – Rechnungen, Finanzberichte
- **Tools & Utilities** – Import/Export, Wartung

## Open-Source Plugins

Kostenlose Plugins sind im offiziellen Repository verfügbar:
[https://github.com/Byte-StoreDE/ByteSuite-Plugins](https://github.com/Byte-StoreDE/ByteSuite-Plugins)

## Preismodelle

- **free** – Kostenlos, Open-Source
- **paid** – Bezahltes Plugin
- **freemium** – Kostenlose Basisversion mit bezahlten Erweiterungen
