# 3. Netlify verbinden

Mit Netlify stellst du Jubla Reporting online zur Verfügung. Dadurch kannst du die App für deine Schar einfach nutzen, ohne selbst einen eigenen Server betreiben zu müssen.

---

## Netlify-Konto erstellen

Falls du noch kein Konto hast: [netlify.com](https://www.netlify.com/) → **«Sign up»** (kostenlos, z.B. mit GitHub-Login)

---

## Repo mit Netlify verbinden

1. Im Netlify-Dashboard: **«Add new site»** → **«Import an existing project»**
2. Wähle **«GitHub»** als Quelle
3. Autorisiere Netlify für deinen GitHub-Account
4. Wähle dein geforktes Repo (z.B. `jubla-wald-reporting`)
5. Build-Einstellungen:

| Einstellung | Wert |
|---|---|
| Branch | `main` |
| Build command | *(leer lassen)* |
| Publish directory | `.` |

6. Klicke auf **«Deploy site»**

!!! info "Erste Deployment fehlerhaft?"
    Das erste Deployment wird wahrscheinlich fehlschlagen, weil die Umgebungsvariablen noch fehlen. Das ist normal – diese richtest du im nächsten Schritt ein.

---

## Eigene Domain (optional)

Netlify vergibt dir automatisch eine Adresse wie `jubla-wald-reporting.netlify.app`. Du kannst diese später unter **«Domain settings»** mit einer eigenen Domain verknüpfen.

---

Weiter zu: [4. Umgebungsvariablen →](umgebungsvariablen.md)
