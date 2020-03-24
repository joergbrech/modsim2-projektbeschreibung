# Modellbildung und Simulation 2 - Ausarbeitung

![CI](https://github.com/joergbrech/modsim2-ausarbeitung/workflows/CI/badge.svg)

:loudspeaker: **Lesen Sie dieses Dokument vollständig bis zum Ende!** :loudspeaker:

Dies ist der Starter Code für ihre Ausarbeitung.  Die Ordnerstruktur ist wie folgt:

|  Ordner   |  Beschreibung   |
| --- | --- |
| `docs` | Latex-Dateien für die Projektdokumentation |
| `src`  | Alle Quelldateien ihrer entwickelten Programme |
| `tests` | *Optional:* Unit tests für ihre entwickelten Funktionen in `src` |
| `.github/workflows` | Skript für Continuous integration (siehe unten). Hier müssen Sie nichts ändern. |

Mit Ausnahme von `.github/workflows` enhalten alle Ordner Beispieldateien, die sie nach Belieben löschen oder abändern können. Die *Ordnerstruktur* sollte aber erhalten bleiben.

## Abgabe

**Wichtig:** Die Abgabe Ihrer Ausarbeitung erfolgt über den Issue Tracker dieses repositories. Erstellen Sie _vor Ablauf ihrer Deadline_ ein Issue, in dem Sie ihre **kompilierte Projektbeschreibung als Anhang beifügen** und mir (@joergbrech) das Issue zur Bearbeitung zuweisen.

Folgende Bedingungen müssen zusätzlich erfüllt sein:

 - :pencil2: Ändern Sie den Titel dieser `README.md` Datei entsprechend ihres Projekttitels um. 

 - :clipboard: Kopieren Sie ihre Projektbeschreibung aus der vorherigen Aufgabe in dieses Repository.

 - :speech_balloon: Der Quellcode muss gut dokumentiert und fehlerfrei ausführbar sein.

 - :exclamation: Der Latexcode muss kompilierbar sein.


## Zusatzinformationen


<details>
<summary>Teamarbeit mit GIT</summary>

### Der Pull-Request Workflow

Sie arbeiten gemeinsam als Team an einem Projekt. Es empfiehlt sich vorab die Aufgaben zu verteilen. Der Issue Tracker bietet sich hier als unterstützendes Tool an.

Damit es möglichst zu wenigen Konflikten kommt, bietet es sich an, die Aufgaben so zu verteilen, dass man sich möglichst wenig in die Quere kommt. Am besten arbeitet ihr, in dem ihr **nur in seltenen Ausnahmen** direkt in den `master` branch commitet. Idealerweise folgt ihr dem Workflow mit Pull Requests:

Angenommen Maja möchte eine bestimmte Teilaufgabe bearbeiten, z.B. das Kapitel "Stand der Technik" in die Projektdokumentation einfügen.

 - Maja wechselt in ihrer lokalen Kopie des repositories auf den `master` branch und sorgt dafür, dass sie alle aktuellen Änderungen aus dem Github repository enthält:

   ```bash
   git checkout master
   git pull
   ```

 - Sie erstellt einen neuen lokalen branch mit einem sprechenden Namen, z.B. `maja/chapter-stand-der-technik`, und welchselt in diesen branch

    ```bash
    git checkout -b maja/chapter-stand-der-technik
    ```

 - Anschließend kann Maja Dateien ändern oder neue hinzufügen, und jede inkrementelle Änderung *commit*en.

    ```bash
    git add 02_stand_der_technik.tex
    git add main.tex
    git commit -m "Stand der Technik Kapitel geschrieben"
    ```

 - Sie kann jederzeit ihre lokalen Änderungen auf das Github repository *push*en. 
   Der Befehl

    ```bash
    git push -u origin HEAD
    ```

    erstellt einen neuen branch im *remote* Github repository mit dem selben Namen wie ihr lokaler branch. Wenn Sie weitere Änderungen an dem branch vornehmen möchte, muss sie beim nächsten mal nur noch 

    ```bash
    git push
    ```

    eingeben, da es schon im *remote* Github repository einen branch mit demselben Namen gibt.

 - Sobald Maja mit der Bearbeitung ihrer Teilaufgabe fertig ist, kann sie auf Github eine *Pull Request* stellen, und einen ihrer Teammitglieder, Peter, um einen *review* bitten. Wenn Peter mit Majas Änderungen einverstanden ist, kann er den *Pull Request* in den `master` branch *mergen*.

  - Sobald Maja's Änderungen im `master` übernommen sind, kann der branch `maja/chapter-stand-der-technik` ohne Bedenken gelöscht werden.

  - Falls Maja eine Aufgabe bearbeitet hat, die im Issue Tracker hinterlegt ist, kann das Issue als erledigt markiert werden.

</details>

<details>

<summary>Was gehört unter Versionskontrolle und was nicht.</summary>

### Stellen Sie folgende Dateien unter Versionskontrolle:

 - Alle von Menschen lesbare Dateien (ASCII), die sie zur Bearbeitung ihres Projektes erstellt haben. Das sind zum Beispiel `*.tex` Dateien oder `*.m` Dateien.
 - Binäre Dateien wie Bilder, die sie in ihrer Dokumentation verwenden.

### Stellen Sie folgende Dateien **nicht** unter Versionskontrolle:

 - Alle automatisch erstellten Dateien. Bei Latex sind das zum Beispiel Dateien mit der Endung `*.aux` oder `*.tmp`.
 - Große binäre Dateien, die sich regelmäßig ändern. **Dazu gehört die PDF-Version ihrer Dokumentation**. Unter Versionskontrolle gehören nur die `*.tex` Dateien, die sie brauchen um das Dokument zu kompilieren. Das Kompilieren des Dokumentes kann jedes Teammitglied lokal machen, oder er kann sich das automatisch erstellte Dokument unter dem Reiter *Actions* herunterladen, siehe "Automatische Tests".

</details>

<details>

<summary>Automatische Tests</summary>

### Continuous Integration

Dieses repository ist so vorbereitet, dass mit jedem *push* und jedem *Pull Request* zwei Aktionen automatisiert in der cloud durchgeführt werden, zum Einen wird das PDF-Dokument kompiliert, und zum anderen werden automatisch unit tests für den Matlab Code durchgeführt. Diese automatisierten Aktionen sind wesentliche Bestandteile von [Continuous Integration](https://de.wikipedia.org/wiki/Kontinuierliche_Integration).

#### Automatisches Erstellen der Projektdokumentation

Das Latex-Dokument wird automatisch online erstellt. Voraussetzung hierf"ur ist, dass der Dokument der Hauptdatei `main.tex` lautet. Das kompilierte Dokument können Sie sich als Artefakt herunterladen, indem Sie unter dem Reiter *Actions* den entsprechenden *commit* anklicken.

#### Automatische unit tests.

Diese Funktionalität ist **optional aber empfohlen**. Da die meisten von Ihnen Matlab-Code intwickeln werden, enthält das repository zu Beginn beispielhaft eine Matlabfunktion `src/fac.m` und eine Testdatei `tests/test_fac.m`. Letztere überprüft, ob die Funktion `fac` das erwartete Ergebnis liefert. Ich lege Ihnen nahe, ihren Code durch viele kleine Funktionen abzubilden, und jeder der Funktionen in einer Datei `tests/test_funktionsname.m` auf ihre Richtigkeit zu überprüfen.

 - `src/fac.m` und `tests/test_fac.m` sind Beispieldateien, um Ihnen die Funktionsweise zu demonstrieren. Sie können bedenkenlos gelöscht werden.
 - Die Unit tests werden mit [MOxUnit](https://github.com/MOxUnit/MOxUnit) durchgeführt, einem *unit testing framework* das mit Matlab und Octave kompatibel ist. Um Tests lokal auf ihrem Rechner durchführen zu können, installieren Sie zunächst [MOxUnit](https://github.com/MOxUnit/MOxUnit).

    Um die unit tests lokal durchzuführen, wechseln Sie in Matlab/Octave in den `src` Ordner und geben 

    ```matlab
    moxunit_runtests('../tests')
    ```

    in das Kommandofenster ein. Damit werden alle Unit tests durchgeführt, die im Verzeichnis `tests` hinterlegt sind.

 - Falls sie sich für eine andere Sprache als Matlab entschieden haben, können Sie ebenfalls unit tests benutzen. In diesem Fall sprechen Sie mich an, ich helfe Ihnen gerne dabei.

</details>

## Nützliche Links

 - [Git Cheatsheet](https://github.github.com/training-kit/downloads/github-git-cheat-sheet.pdf)
 - [Markdown Cheatsheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet)
 - [Markdown Emoticons](https://gist.github.com/rxaviers/7360908)
