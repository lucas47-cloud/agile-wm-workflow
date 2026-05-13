# Agile WM Workflow

**KI-gestütztes Wissensmanagement & Tool-Entscheidung**

Eine statische Webapp die den kombinierten Workflow aus WM (Claude Project) und Juri (Custom GPT) interaktiv abbildet.

---

## Was die App kann

- **WM-Formular** – Unternehmenskontext eingeben → fertigen Analyse-Prompt für Claude generieren
- **Scoring Matrix** – Tool-Kandidaten nach 4 Kriterien bewerten + optionaler Compliance-Score
- **Juri-Übergabe** – fertigen Übergabe-Prompt für Juri (Custom GPT) generieren

---

## Auf Live-Modus umstellen

Nur zwei Zeilen in `index.html` ändern:

```javascript
const WMService = {
  mode: 'live',          // 'static' → 'live'
  apiKey: 'sk-ant-...',  // Claude API Key eintragen
  ...
}
```

Fertig. Der Rest des Codes bleibt unverändert.

---

## GitHub Pages deployen

1. Repository auf GitHub erstellen
2. `index.html` und `README.md` pushen
3. Settings → Pages → Branch: `main` → `/root`
4. App läuft unter `https://[username].github.io/[repo-name]`

---

## Pilotunternehmen

Buildwise GmbH · Bauplanung · München · 28 MA · Kanban als Einstieg

---

## Workflow

```
🖐 Nutzer gibt Firmendaten ein
        ↓
🤖 WM (Claude Project) analysiert
        ↓
📊 Berater/Team führt Scoring durch
        ↓
⚖️ Juri (Custom GPT) analysiert ToS
        ↓
📄 Berater führt Report zusammen
```
