# Satzungsrepository – 1st Aircat Division

## Zweck dieses Repositories

Dieses Repository dient der zentralen, nachvollziehbaren und versionssicheren Verwaltung der Satzung der 1ACD.

Es verfolgt dabei folgende Ziele:

- Bereitstellung der **aktuellen, beschlossenen Satzung** als PDF  
- Nachvollziehbare **Historie aller Änderungen**  
- Strukturierte **Bearbeitung von Änderungsvorschlägen**  
- Transparenz für alle Mitglieder – auch ohne technische Vorkenntnisse  

Die Verwaltung erfolgt über Git und GitHub, wodurch jede Änderung dokumentiert und dauerhaft nachvollziehbar ist.

## Wichtiger Hinweis

Diese README wurde mithilfe von Künstlicher Intelligenz erstellt.

# Aktuelle Satzung einsehen

Die aktuell gültige Version der Satzung ist **nicht im Quellcode**, sondern als PDF hinterlegt.

## So findest du sie:

1. Öffne das Repository im Browser  
2. Klicke auf den Bereich **„Releases“**  
3. Wähle den neuesten Eintrag (oberster Eintrag)  
4. Lade die PDF-Datei herunter  

👉 Diese PDF ist die **offiziell beschlossene Version der Satzung**

# Historie der Satzung ansehen

Alle früheren Versionen sind ebenfalls verfügbar.

## Möglichkeit 1: Über Releases (empfohlen)

- Jeder Release entspricht einem offiziellen Stand  
- Enthält jeweils die passende PDF  

👉 Einfach ältere Releases öffnen und vergleichen

## Möglichkeit 2: Über den Quellcode

1. Gehe auf **„Commits“**  
2. Wähle einen Zeitpunkt aus  
3. Sieh dir die Änderungen im Detail an  

👉 Hier siehst du genau, **was sich geändert hat**

# Änderungsvorschläge ansehen

Änderungsvorschläge werden nicht mehr als Ordner gespeichert, sondern als sogenannte **Branches**.

## So findest du Vorschläge:

1. Gehe auf die Branch-Auswahl (oben links im Repository)  
2. Wähle einen Branch mit dem Namen:

```
vorschlag-YYYY-MM-DD
```

3. Öffne die Datei `src/satzung.tex`

👉 Das ist der vollständige Vorschlag


## Änderungen im Vergleich sehen

1. Öffne den entsprechenden Branch  
2. Klicke auf „Compare“ oder „Pull Request“ (falls vorhanden)  

👉 Du siehst direkt:
- alte Version vs. neue Version  
- alle Änderungen hervorgehoben  

# LaTeX-Quellcode ansehen

Die Satzung wird in LaTeX geschrieben.

## Datei:

```
src/satzung.tex
```

Diese kannst du direkt im Browser öffnen und lesen.

# LaTeX lokal bearbeiten

Wenn du selbst Änderungen vornehmen möchtest, kannst du das lokal auf deinem Rechner tun.


## Voraussetzungen

- Git installiert  
- LaTeX-Distribution installiert  

## 1. Repository herunterladen

### Windows / macOS / Linux

Im Terminal oder in der Konsole:

```bash
git clone <Repository-URL>
cd <Repository-Name>
```

## 2. Datei bearbeiten

Öffne:

```
src/satzung.tex
```

mit einem Editor deiner Wahl:

### Windows
- Notepad++
- VS Code

### macOS
- TextEdit (einfach)
- VS Code
- MacTeX Editor

### Linux
- VS Code
- nano / vim
- TeXstudio

## 3. PDF erstellen

### Windows
```bash
pdflatex src/satzung.tex
```

### macOS
```bash
pdflatex src/satzung.tex
```

### Linux
```bash
pdflatex src/satzung.tex
```

👉 Die PDF wird im gleichen Ordner erzeugt

# Eigene Vorschläge einbringen (einfach erklärt)

Wenn du Änderungen vorschlagen möchtest:

1. Repository herunterladen  
2. Änderungen in `satzung.tex` machen  
3. neuen Branch erstellen  
4. Änderungen hochladen  

(Details dazu werden separat dokumentiert)

# Grundprinzip dieses Systems

- **Offizielle Versionen** = Releases + PDF  
- **Änderungen** = Commits  
- **Vorschläge** = Branches  
- **Beschlüsse** = Zusammenführung (Merge)  

# Warum dieses System?

Im Vergleich zur alten Ordnerstruktur:

| Alt | Neu |
|-----|-----|
| viele Kopien | eine zentrale Quelle |
| hoher Speicherverbrauch | nur Änderungen gespeichert |
| schwer nachvollziehbar | vollständige Historie |
| manuelle Organisation | strukturierter Workflow |

# Unterstützung

Falls du mit Git oder GitHub nicht vertraut bist:

- Nutze primär die **Releases (PDFs)**  
- oder wende dich an technisch erfahrene Mitglieder  


Dieses Repository ist so aufgebaut, dass sowohl technische als auch nicht-technische Nutzer damit arbeiten können.
