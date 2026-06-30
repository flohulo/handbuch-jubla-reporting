# 2. Google Sheets einrichten

Google Sheets ist die zentrale Tabelle, in der alle Berichte und Einträge für deine Schar gesammelt werden. So brauchst du keine eigene Datenbank zu pflegen.

---

## Google Sheet erstellen

1. Gehe zu [sheets.google.com](https://sheets.google.com) und erstelle eine neue Tabelle
2. Benenne sie z.B. `Jubla Reporting – [Scharname]`
3. Richte die Tabs (Tabellenblätter) gemäss der folgenden Struktur ein

---

## Tab-Struktur

Das Sheet muss **mindestens zwei Tabs** enthalten:

### Tab 1: `Berichte`

Hier landen alle eingereichten Gruppenstunden-Berichte. Die Spalten müssen in dieser Reihenfolge angelegt werden:

| Spalte | Inhalt |
|--------|--------|
| A | Zeitstempel |
| B | Datum der Gruppenstunde |
| C | Schar / Gruppe |
| D | Leitende Person |
| E | Anzahl Teilnehmende |
| F | Thema / Aktivität |
| G | Verlauf (Freitext) |
| H | Besondere Vorkommnisse |
| I | Alarm ausgelöst (ja/nein) |

!!! warning "Spaltenreihenfolge nicht ändern"
    Die Reihenfolge der Spalten ist fix definiert. Wenn du Spalten verschiebst, funktioniert das Tool nicht mehr korrekt.

### Tab 2: `Strikes`

Für die Strike-Erfassung bei Verhaltensauffälligkeiten:

| Spalte | Inhalt |
|--------|--------|
| A | Zeitstempel |
| B | Datum |
| C | Name der Person |
| D | Beschreibung |
| E | Eingetragen von |

---

## Google API aktivieren

Damit jubla-reporting auf dein Sheet schreiben darf, musst du die **Google Sheets API** aktivieren und einen Service Account erstellen:

1. Öffne die [Google Cloud Console](https://console.cloud.google.com/)
2. Erstelle ein neues Projekt (z.B. `jubla-reporting`)
3. Gehe zu **«APIs & Dienste»** → **«Bibliothek»**
4. Suche nach `Google Sheets API` und aktiviere sie
5. Gehe zu **«APIs & Dienste»** → **«Anmeldedaten»**
6. Klicke auf **«Anmeldedaten erstellen»** → **«Dienstkonto»**
7. Vergib einen Namen (z.B. `jubla-reporting-bot`) und klicke auf **«Fertig»**
8. Öffne das erstellte Dienstkonto → Tab **«Schlüssel»** → **«Schlüssel hinzufügen»** → **«JSON»**
9. Die heruntergeladene JSON-Datei enthält alle Werte für deine [Umgebungsvariablen](umgebungsvariablen.md)

### Sheet freigeben

Damit der Service Account auf dein Sheet zugreifen kann:

1. Öffne dein Google Sheet
2. Klicke auf **«Freigeben»**
3. Füge die **E-Mail-Adresse des Dienstkontos** hinzu (Format: `name@projektid.iam.gserviceaccount.com`)
4. Berechtigung: **«Bearbeiter»**

---

## Sheet-ID notieren

Die Sheet-ID findest du in der URL deines Sheets:

```
https://docs.google.com/spreadsheets/d/DEINE_SHEET_ID/edit
```

Du brauchst sie später für die Umgebungsvariablen.

---

Weiter zu: [3. Netlify verbinden →](netlify.md)
