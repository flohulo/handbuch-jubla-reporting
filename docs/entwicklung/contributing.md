# Mitwirken (Contributing)

Jubla Reporting ist ein Open-Source-Projekt und lebt von der Mitarbeit der Community. Jeder Beitrag ist willkommen!

---

## Wie kann ich helfen?

### 🐞 Bugs melden
Hast du einen Fehler gefunden? Erstelle ein [GitHub Issue](https://github.com/flohulo/jubla-reporting/issues) mit:
- Beschreibung des Fehlers
- Schritte zur Reproduktion
- Screenshots (falls hilfreich)
- Gerät und Browser

### 💡 Feature vorschlagen
Idee für eine neue Funktion? Auch dafür gibt es [GitHub Issues](https://github.com/flohulo/jubla-reporting/issues). Beschreibe kurz:
- Was soll die Funktion tun?
- Für wen ist sie nützlich?

### 🔧 Code beitragen
1. Forke das Repo
2. Erstelle einen neuen Branch: `git checkout -b feature/mein-feature`
3. Schreibe deinen Code und committe: `git commit -m "feat: mein Feature beschreiben"`
4. Push: `git push origin feature/mein-feature`
5. Erstelle einen **Pull Request** auf GitHub

!!! info "Commit-Konventionen"
    Wir verwenden [Conventional Commits](https://www.conventionalcommits.org/): `feat:`, `fix:`, `docs:`, `chore:` etc.

---

## Lokale Entwicklungsumgebung

```bash
# Repo klonen
git clone https://github.com/flohulo/jubla-reporting.git
cd jubla-reporting

# Abhängigkeiten installieren
npm install

# Netlify CLI installieren (falls noch nicht vorhanden)
npm install -g netlify-cli

# Lokal starten (mit Netlify Dev für Functions)
netlify dev
```

Erstelle eine `.env`-Datei im Root-Verzeichnis mit allen [Umgebungsvariablen](../einrichtung/umgebungsvariablen.md).

---

## Veröffentlichung

Neue Versionen werden durch das Erstellen eines **GitHub Release** veröffentlicht. Das Versionierungsschema folgt [Semantic Versioning](https://semver.org/lang/de/): `MAJOR.MINOR.PATCH`
