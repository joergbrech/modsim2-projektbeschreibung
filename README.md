# Modellbildung und Simulation 2 - Projektbeschreibung

![CI](https://github.com/joergbrech/modsim2-ausarbeitung/workflows/CI/badge.svg)

:loudspeaker: **Lesen Sie dieses Dokument vollständig bis zum Ende!** :loudspeaker:


## Inhalt der Aufgabe

 - Sie demonstrieren, dass Sie mit git vertraut sind.
 - Sie erhalten Einblick in automatisierte Software-Tests
 - Sie verfassen eine Projektbeschreibung für Ihre Ausarbeitung


## Abgabe

**Wichtig:** Die Abgabe dieser Übung erfolgt über den Issue Tracker dieses repositories sowie mittels Pull Request. 

 1. Erstellen Sie _mit genügend Puffer vor Ablauf ihrer Deadline_ ein Issue mit dem Titel `Projektbeschreibung absegnen` und weisen es mir (@joergbrech) zur Bearbeitung zu. 
 2. Erstellen Sie einen *Pull Request*, der den Bug in `src/fac.m` behebt und verlangen von mir (@joergbrech) ein *review*.

:point_right: **Erst wenn ich explizit die Projektbeschreibung sowie den Pull Request abgesegnet habe, gilt die Aufgabe als bestanden! Das Erstellen des Issues und des PRs alleine reicht nicht!** :point_left:

## Ihre Aufgabe

TODO: Hier VIEL ausführlicher.

 - Machen Sie sich mit dem System [git](https://git-scm.com/) vertraut.
 - Erstellen Sie ein Issue
 - Erstellen Sie ein branch `factorial-bug`. Reparieren Sie den Programmierfehler, der sich in `src/fac.m` eingeschlichen hat und stellen Sie einen Pull Request.
 - Füllen Sie die fehlenden Inhalte in `PROJEKTBESCHREIBUNG.md` aus.

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
 - Große binäre Dateien, die sich regelmäßig ändern.

</details>

<details>

<summary>Automatische Tests</summary>

### Continuous Integration

Dieses repository ist so vorbereitet, dass mit jedem *push* und jedem *Pull Request* Aktionen automatisiert in der cloud durchgeführt werden, konkret werden unit tests für den Matlab Code in `src` durchgeführt. Diese automatisierten Aktionen sind wesentliche Bestandteile von [Continuous Integration](https://de.wikipedia.org/wiki/Kontinuierliche_Integration).


</details>

## Nützliche Links

 - [Git Cheatsheet](https://github.github.com/training-kit/downloads/github-git-cheat-sheet.pdf)
 - [Markdown Cheatsheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet)
 - [Markdown Emoticons](https://gist.github.com/rxaviers/7360908)
