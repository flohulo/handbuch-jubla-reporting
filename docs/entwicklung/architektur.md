# Architektur

Jubla Reporting ist eine **serverlose Webanwendung**, die auf drei externe Dienste setzt:

```
Browser (Frontend)
      │
      │ HTTP-Request
      ▼
Netlify Functions (Backend)
      │                │
      │                │
      ▼                ▼
Google Sheets       SMTP-Server
  (Daten)           (Alarm-Mails)
```

---

## Komponenten

### Frontend
- Statisches HTML/CSS/JavaScript
- Mobile-first Design
- Wird direkt über Netlify CDN ausgeliefert
- Konfiguration via `config.js`

### Netlify Functions
Serverlose Node.js-Funktionen, die im Hintergrund laufen:

| Funktion | Aufgabe |
|---|---|
| `submit-report` | Bericht ins Google Sheet schreiben |
| `submit-strike` | Strike ins Google Sheet schreiben |
| `send-alarm` | Alarm-Mail via SMTP versenden |
| `get-report` | Auszug aus dem Sheet abrufen |

### Google Sheets
- Dient als Datenbank
- Kein eigener Server nötig
- Daten via Google Sheets API geschrieben und gelesen

### SMTP / E-Mail
- Nodemailer für den Mail-Versand
- Kompatibel mit jedem SMTP-Server (Gmail, Outlook, etc.)

---

## Tech-Stack

| Bereich | Technologie |
|---|---|
| Hosting | Netlify |
| Backend (Funktionen) | Netlify Functions (Node.js) |
| Datenbank | Google Sheets API |
| E-Mail | Nodemailer / SMTP |
| PDF-Generierung | jsPDF |
| Lizenz | GPL-3.0 |
