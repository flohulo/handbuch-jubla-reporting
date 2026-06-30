# 4. Umgebungsvariablen

Umgebungsvariablen sind die geheimen Zugangsdaten, die Jubla Reporting braucht, damit die App mit Google Sheets und E-Mails korrekt arbeiten kann. Sie werden sicher in Netlify hinterlegt.

---

## Variablen in Netlify hinterlegen

1. Öffne dein Projekt im Netlify-Dashboard
2. Gehe zu **«Site configuration»** → **«Environment variables»**
3. Klicke auf **«Add a variable»**
4. Füge alle unten aufgelisteten Variablen einzeln hinzu

---

## Übersicht aller Variablen

### Google Sheets

Diese Werte findest du in der JSON-Datei deines Google Service Accounts (aus Schritt 2):

| Variable | Beschreibung | Wo finden? |
|---|---|---|
| `GOOGLE_SERVICE_ACCOUNT_EMAIL` | E-Mail-Adresse des Dienstkontos | Feld `client_email` in der JSON-Datei |
| `GOOGLE_PRIVATE_KEY` | Privater Schlüssel | Feld `private_key` in der JSON-Datei |
| `SPREADSHEET_ID` | ID deines Google Sheets | Aus der Sheet-URL (siehe [Schritt 2](google-sheets.md)) |

!!! warning "Private Key korrekt kopieren"
    Der `GOOGLE_PRIVATE_KEY` enthält Zeilenumbrüche (`\n`). Kopiere den gesamten Wert inklusive `-----BEGIN PRIVATE KEY-----` und `-----END PRIVATE KEY-----`.

### E-Mail (Alarm-Funktion)

Für den Versand von Alarm-E-Mails bei kritischen Vorfällen:

| Variable | Beschreibung |
|---|---|
| `SMTP_HOST` | SMTP-Server deines Mail-Anbieters (z.B. `smtp.gmail.com`) |
| `SMTP_PORT` | Port (meistens `587` für TLS) |
| `SMTP_USER` | E-Mail-Adresse, von der gesendet wird |
| `SMTP_PASS` | Passwort / App-Passwort |
| `ALARM_RECIPIENT` | E-Mail-Adresse der Scharleitung, die Alarm-Mails erhält |

!!! tip "Gmail App-Passwort"
    Wenn du Gmail verwendest, musst du ein **App-Passwort** erstellen (kein normales Gmail-Passwort). Das geht unter: [Google-Konto](https://myaccount.google.com/) → Sicherheit → 2-Schritt-Verifizierung → App-Passwörter.

---

## Deployment neu starten

Nach dem Hinterlegen aller Variablen:

1. Netlify-Dashboard → **«Deploys»**
2. **«Trigger deploy»** → **«Deploy site»**

Das Deployment sollte nun erfolgreich sein. ✅

---

Weiter zu: [5. Branding & Konfiguration →](branding.md)
