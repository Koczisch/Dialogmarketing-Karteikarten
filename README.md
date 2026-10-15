[README.md](https://github.com/user-attachments/files/33489931/README.md)
# Karteikasten Dialogmarketing

Lernmaterial zur Vorbereitung auf die IHK-Abschlussprüfung **Kaufmann/Kauffrau für Dialogmarketing**. Grundlage sind die Prüfungen von drei Terminen:

- Sommer 2024
- Winter 2023/24
- Winter 2024/25

Aus diesen Prüfungen sind 255 Karteikarten entstanden. Jede Karte hat eine Frage auf der Vorderseite und eine Antwort auf der Rückseite. Die Karten gibt es in zwei Formen:

1. **Als interaktive Lernseite** (`karteikarten.html`) zum Lernen im Browser
2. **Als CSV-Datei** (`Karteikarten_Dialogmarketing.csv`) zum Import in Anki oder ein anderes Karteikartenprogramm

## Ausgewertete Prüfungen

| Prüfungsteil | Format | Termine | Offizielle Lösung |
|---|---|---|---|
| Projektmanagement im Dialogmarketing (PM) | 4–7 offene Aufgaben, 150 Min. | S24, W23, W24 | nein |
| Gestaltung und Vertrieb von Dienstleistungen (GuV) | 30 Aufgaben, 60 Min. | S24, W23, W24 | ja |
| Wirtschafts- und Sozialkunde (WiSo) | 30 Aufgaben, 60 Min. | S24, W23, W24 | ja |

Insgesamt sind das 9 verschiedene Prüfungsteile und 3 Lösungsbögen der IHK. Drei hochgeladene Dateien waren Duplikate oder zweite Scans derselben Prüfung. Sie wurden nur einmal gezählt.

## Dateien

| Datei | Inhalt |
|---|---|
| `cards.py` | Alle Karten als Daten (Thema, Priorität, Frage, Antwort, Quelle). Inhalte werden nur hier bearbeitet. |
| `template.html` | Vorlage der Lernseite (Gestaltung und Funktionen) mit dem Platzhalter `__DATA__` |
| `build.py` | Erzeugt aus `cards.py` die Lernseite und die CSV-Datei |
| `karteikarten.html` | Fertige Lernseite (wird erzeugt, nicht von Hand bearbeiten) |
| `Karteikarten_Dialogmarketing.csv` | Fertige Importdatei für Anki (wird erzeugt) |

## Aufbau der Karten

Jede Karte hat diese Felder:

- **Thema:** eines von 18 Themengebieten
- **Priorität:** A, B oder C
- **Frage** (Vorderseite) und **Antwort** (Rückseite)
- **Quelle:** die Prüfungsaufgabe, aus der die Karte stammt

### Themengebiete

| Prüfungsteil | Themen |
|---|---|
| Projektmanagement | Kennzahlen im Service-Center · Personal- & Kapazitätsplanung · Kalkulation · Kosten- & Leistungsrechnung · Projektmanagement · Personalwesen & Arbeitsschutz |
| Gestaltung und Vertrieb | Team, Führung & Kommunikation · Markt & Marketing · Verkauf & Kundenbeziehung · IT, Datenbanken & Datenschutz |
| WiSo | Vertragsrecht · Rechtsformen · Arbeitsrecht & Mitbestimmung · Sozialversicherung & Steuern · Markt & Preisbildung · Wirtschaftsordnung & Wettbewerb · Konjunktur & Wirtschaftspolitik · Nachhaltigkeit & Recycling |

Innerhalb eines Themas stehen zuerst die Grundbegriffe, danach Zusammenhänge, Rechenaufgaben und typische Fehlerquellen.

### Prioritäten

Die Priorität wurde aus den vorliegenden Prüfungen abgeleitet.

| Priorität | Bedeutung | Anzahl |
|---|---|---|
| **A** | Kam in mehreren Prüfungen vor oder ist Grundlage für viele Aufgaben | 156 |
| **B** | Wichtige Ergänzung, häufiger Anwendungsfall | 84 |
| **C** | Detailwissen, nur einmal geprüft | 15 |

Die Prioritäten sind keine Vorhersage, was in der nächsten Prüfung drankommt.

### Quellenkürzel

Ein Beispiel: `W23 GuV 11` bedeutet Winter 2023/24, Prüfungsteil Gestaltung und Vertrieb, Aufgabe 11.

- **S24** = Sommer 2024, **W23** = Winter 2023/24, **W24** = Winter 2024/25
- **PM** = Projektmanagement, **GuV** = Gestaltung und Vertrieb, **WiSo** = Wirtschafts- und Sozialkunde

## Die Lernseite benutzen

Öffne `karteikarten.html` im Browser oder über den veröffentlichten Link. Die Seite hat drei Bereiche.

**Lernen**
- Karte anklicken oder die Leertaste drücken, um sie umzudrehen
- Mit **Nochmal** oder **Gewusst** deinen Stand markieren
- Nach Thema und Priorität filtern
- „Nur ‚Nochmal‘ und neue“ zeigt nur Karten, die du noch nicht kannst
- **Mischen** ändert die Reihenfolge zufällig, **Sortiert** stellt die Lernreihenfolge wieder her

Tastenkürzel:

| Taste | Aktion |
|---|---|
| Leertaste | Karte umdrehen |
| ← / → | vorherige / nächste Karte |
| 1 | Nochmal |
| 2 | Gewusst |

**Alle Karten**
Eine Tabelle mit allen Karten und einer Suche (z. B. „Ausschöpfung“, „AGB“, „Lohnquote“).

**Übersicht**
Ausgewertete Prüfungen, Kartenzahl je Thema, wiederkehrende Inhalte und bekannte Lücken.

Der Lernfortschritt wird nur im eigenen Browser gespeichert. Auf einem anderen Gerät, in einem privaten Fenster oder nach dem Löschen der Browserdaten ist er nicht mehr vorhanden.

## Import in Anki

1. In Anki **Datei → Importieren** wählen und `Karteikarten_Dialogmarketing.csv` auswählen
2. Als Trennzeichen **Komma** einstellen
3. **HTML in Feldern erlauben** aktivieren, damit Zeilenumbrüche richtig angezeigt werden
4. Die erste Zeile enthält die Spaltennamen. Sie bei Bedarf überspringen.
5. Felder zuordnen: Frage → Vorderseite, Antwort → Rückseite. Thema und Priorität können als Schlagwörter (Tags) oder als eigene Felder übernommen werden.

Die CSV hat die Spalten `Thema`, `Priorität`, `Frage` und `Antwort`. Die Quelle steht am Ende der Antwort.

## Karten ändern oder ergänzen

1. Die Karte in `cards.py` bearbeiten oder neu anlegen:
   ```python
   C(T, "A", "Frage?", "Antwort.\nZweite Zeile.", "S24 PM 1.2")
   ```
   `T` ist das Thema des jeweiligen Abschnitts. `\n` erzeugt einen Zeilenumbruch.
2. Lernseite und CSV neu erzeugen:
   ```bash
   python3 build.py
   ```
3. Die Nummern der Karten werden automatisch in der Reihenfolge von `cards.py` vergeben.

Benötigt wird nur Python 3, keine zusätzlichen Pakete. Die Lernseite lädt Schriften von Google Fonts. Ohne Internetverbindung werden Systemschriften verwendet.

## Hinweise zur Qualität

- **Projektmanagement:** Für diese drei Prüfungen gab es keine offiziellen Lösungen. Die Antworten sind eigene Musterlösungen. Alle Rechnungen wurden nachgerechnet.
- **GuV und WiSo:** Die Antworten folgen den Lösungsbögen der IHK.
- **Abbildungen:** Einige Aufgaben hängen an Abbildungen, die im Scan nicht lesbar waren (GuV S24 A6, GuV W23 A17 und A28, GuV W24 A20 und A28, WiSo W23 A19). Dazu gibt es Karten zum Prinzip, aber nicht zur konkreten Abbildung.
- **Nicht gewertet:** WiSo W24 A8 wurde von der IHK nicht gewertet („Keine Auswertung“).
- **Zwei richtige Lösungen:** Bei GuV S24 A12 akzeptiert die IHK 0,5 (Prozentpunkte) oder 3,3 (Prozent).
- **Aktuelle Werte:** Beträge wie der Arbeitnehmer-Pauschbetrag oder die Beitragsbemessungsgrenzen ändern sich. Vor der Prüfung den aktuellen Stand prüfen.

## Urheberrecht

Die Prüfungsaufgaben und Lösungen sind urheberrechtlich geschützt (© IHK Nürnberg für Mittelfranken, AkA). Die Karten fassen den Prüfungsstoff zum eigenen Lernen zusammen. Die Originalprüfungen sind nicht enthalten und dürfen nicht weitergegeben werden.
