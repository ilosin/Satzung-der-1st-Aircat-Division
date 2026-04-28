# Beitragsrichtlinien – Satzungsrepository 1st Aircat Division

Dieses Dokument beschreibt, wie Änderungen an der Satzung der 1st Aircat Division vorzunehmen sind.

Es richtet sich an alle Mitglieder, unabhängig von technischen Vorkenntnissen.

## Hinweis zum Arbeits- und Einreichungsprozess

Der in der Satzung vorgesehene Änderungsprozess bleibt jederzeit gültig und kann vollständig unabhängig von diesem technischen System genutzt werden.

Die Nutzung von Git und GitHub stellt lediglich eine unterstützende Möglichkeit dar, um Änderungen strukturiert vorzubereiten, nachzuvollziehen und transparent zu dokumentieren.

Insbesondere dient der GitHub-basierte Workflow als optionale Möglichkeit, die Leitung der 1st Aircat Division darüber zu informieren, dass ein Änderungsvorschlag ausgearbeitet wurde und zur Prüfung oder Abstimmung bereitsteht.

### Einreichung über GitHub (optional)

Die Einreichung eines Änderungsvorschlags erfolgt durch das Arbeiten in einem dedizierten Vorschlags-Branch sowie durch das anschließende Hochladen der Änderungen in dieses Repository.

Typischer Ablauf:

```bash
git add .
git commit -m "Vorschlag: Beschreibung der Änderungen"
git push origin vorschlag-YYYY-MM-DD
```

Dieser Vorgang erstellt keinen Pull Request automatisch.

Ein Pull Request wird anschließend manuell auf [GitHub](https://github.com/ilosin/Satzung-der-1st-Aircat-Division/pulls) erstellt und dient ausschließlich der Information der Leitung über die Fertigstellung eines Vorschlags.

### Wichtiger Grundsatz

- Die Nutzung von GitHub ist **nicht verpflichtend**, sondern ein unterstützendes Werkzeug.
- Alternativ können Vorschläge jederzeit direkt an die Leitung oder andere zuständige administrative Stellen der 1st Aircat Division herangetragen werden.
- Die in der Satzung definierten formalen Wege zur Einbringung, Diskussion und Abstimmung von Änderungen bleiben davon vollständig unberührt und haben Vorrang.

### Integrität des Systems

- Durch das Hochladen eines Vorschlags-Branches kann niemand direkt die offizielle Satzung ändern.
- Änderungen werden ausschließlich durch das in der Satzung festgelegte Verfahren (Abstimmung in einer Mitgliederversammlung) wirksam.
- Jeder Vorschlag stellt somit ausschließlich einen Bearbeitungs-, Entwurfs- oder Diskussionsstand dar.

--- 

## 1. Grundprinzip

Die Satzung wird vollständig über Git verwaltet. Änderungen erfolgen strukturiert über:

- Branches (Vorschläge)
- Commits (Änderungen)
- Tags (beschlossene Stände)
- Releases (veröffentlichte PDF-Versionen)


## 2. Erstellung eines Änderungsvorschlags

Für jede geplante Änderung muss ein eigener Branch erstellt werden.

### Benennung des Branches

Der Branch muss folgendes Format haben:

```
vorschlag-YYYY-MM-DD
```

Dabei ist das Datum der Zeitpunkt, zu dem die Änderung voraussichtlich zur Abstimmung gestellt wird.

### Ausgangspunkt

Neue Vorschläge müssen immer vom aktuellen offiziellen Stand ausgehen:

```bash
git checkout offiziel
git pull
git checkout -b vorschlag-YYYY-MM-DD
```

## 3. Bearbeitung der Satzung

Die Satzung befindet sich im LaTeX-Quellcode:

```
src/satzung.tex
```

### Dokumentationsregeln für Änderungen

Damit Änderungen in der später erzeugten PDF (insbesondere für Abstimmungen) klar und eindeutig erkennbar sind, gelten folgende farbliche Markierungsregeln im LaTeX-Quellcode:

#### 🔴 Inhaltliche Änderungen (ändernder oder entfernender Charakter)
Alle Änderungen, die den Sinn oder Inhalt der Satzung verändern, werden **rot markiert**.

- Neue Inhalte (inhaltlich relevant / Ergänzungen):
```latex
\textcolor{red}{Neuer oder geänderter Inhalt}
```

- Entfallene Inhalte:
```latex
\textcolor{red}{\sout{Entfallener Inhalt}}
```

👉 Ziel: Alle inhaltlichen Änderungen sollen in der Abstimmungs-PDF sofort sichtbar sein.

#### 🟢 Redaktionelle Änderungen
Rein sprachliche oder stilistische Anpassungen ohne inhaltliche Änderung werden **grün markiert**:

```latex
\textcolor{green}{Redaktionell überarbeiteter Text}
```

👉 Beispiele:
- Rechtschreibung
- Satzbau
- Formatierung ohne Bedeutungsänderung

## Ziel dieser Markierungen

Diese Farbkennzeichnung dient dazu, dass in der im Rahmen der Abstimmung erzeugten PDF:

- Änderungen sofort visuell erkennbar sind
- neue Inhalte und gestrichene Inhalte klar hervorgehoben werden
- Diskussionen über Änderungen erleichtert werden
- keine inhaltlichen Änderungen übersehen werden können

## 4. Commit-Regeln

Jede sinnvolle Änderung muss separat committet werden.

### Format:

```
Vorschlag: kurze Beschreibung der Änderung
```

Beispiel:

```
Vorschlag: §7 Abstimmungsverfahren präzisiert
```

## 5. Einreichung eines Vorschlags

```bash
git add .
git commit -m "Vorschlag: Beschreibung der Änderungen"
git push origin vorschlag-YYYY-MM-DD
```

## 6. Beschluss einer Änderung

Wird ein Vorschlag angenommen:

### 6.1 Merge in den offiziellen Stand

```bash
git checkout offiziel
git merge vorschlag-YYYY-MM-DD
```


### 6.2 Tag erstellen (verpflichtend)

Format:

```
stand-YYYY-MM-DD
```


### 6.3 Commit-Nachricht

```
Stand: DD. Monat Jahr
```

Beispiel:

```
Stand: 17. Juni 2025
```

## 7. Veröffentlichung (Release)

Jeder offizielle Stand muss als Release veröffentlicht werden.

### Anforderungen:

- Tag auswählen: `stand-YYYY-MM-DD`
- Titel:
  ```
  Satzung Stand DD. Monat YYYY
  ```
- PDF-Datei hochladen:
  ```
  Satzung_1ACD_Stand_YYYY_MM_DD.pdf
  ```
- Beschreibung:
  - Datum/Zeitraum der Beschlussgebenden Mitgliederversammlung
  - wichtigste Änderungen
  - kurze Zusammenfassung

## 8. Ziel dieses Workflows

- vollständige Nachvollziehbarkeit aller Änderungen
- klare Trennung zwischen Vorschlag und Beschluss
- transparente Zusammenarbeit
- langfristige Stabilität der Satzung

## 9. Hinweis

Alle Änderungen müssen den in der Satzung definierten Verfahren entsprechen.

Nur offiziell beschlossene Änderungen dürfen in den `offiziel`-Branch übernommen werden.
