# 5. Branding & Konfiguration

Jubla Reporting lässt sich ohne Programmierkenntnisse an deine Schar anpassen. Alle wichtigen Einstellungen sind in der Datei `config.js` im Root-Verzeichnis deines Repos zusammengefasst.

---

## Die Datei `config.js`

Öffne die Datei direkt auf GitHub und klicke auf das Stift-Symbol ✏️ zum Bearbeiten.

### Beispiel-Konfiguration

```js
const CONFIG = {
  // Name deiner Schar (erscheint im Header und in E-Mails)
  SCHAR_NAME: "Jubla Wald",

  // Logo-Pfad (lege dein Logo unter /assets/logo.png ab)
  LOGO_PATH: "assets/logo.png",

  // Primärfarbe (Hex-Code)
  PRIMARY_COLOR: "#E87722",

  // Gruppen, die im Dropdown angezeigt werden
  GRUPPEN: [
    "Biber",
    "Wölfe",
    "Pfadis",
    "Rover"
  ],

  // Kontakt für den Hilfe-Link
  KONTAKT_EMAIL: "leitung@jubla-wald.ch"
};
```

---

## Logo einfügen

1. Bereite dein Logo als PNG vor (empfohlene Grösse: 200×200 px, transparenter Hintergrund)
2. Lade es in deinem GitHub-Repo unter `assets/logo.png` hoch
3. Stelle sicher, dass der Pfad in `config.js` korrekt ist

---

## Farben anpassen

Jubla-Farben zur Orientierung:

| Farbe | Hex-Code |
|---|---|
| Jubla Orange | `#E87722` |
| Jubla Dunkelblau | `#1A3A5C` |
| Jubla Hellgrau | `#F5F5F5` |

---

!!! success "Setup abgeschlossen!"
    Wenn du alle fünf Schritte erledigt hast, ist dein Jubla Reporting Tool einsatzbereit. Teile den Link zu deiner Netlify-App mit deinen Leitenden!

Weiter zu: [Nutzung für Leitende →](../nutzung/leitende.md)
