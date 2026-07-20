# AGIT Documentation Template

> [!NOTE]
> **KI-Zusammenarbeit**
>
> Dieses Repository pflegt das AGIT Documentation Template.
>
> Das AGIT Documentation Template ist die dokumentationsorientierte Spezialisierung der AGIT-Template-Familie.
>
> Das Kollaborationsmodell dokumentiert Dokumentationspraktiken, KI-gestützte Dokumentationsworkflows, Link- und visuelle QA-Disziplin sowie Repository-Konventionen für Dokumentationsprojekte.
>
> Das Kollaborationsmodell wird in [ChatGPT.md](ChatGPT.md) gepflegt.

[English documentation](README.md) · Die englische README ist maßgeblich; die deutsche README wird als enge Übersetzung gepflegt.

## Inhalt

- [Überblick](#überblick)
- [Kernprinzip](#kernprinzip)
- [AGIT Templateverse](#agit-templateverse)
- [Wann dieses Template geeignet ist](#wann-dieses-template-geeignet-ist)
- [Projektinitialisierung](#projektinitialisierung)
- [Empfohlene Workflows](#empfohlene-workflows)
- [Git-Index und geschützte Git-Aktionen](#git-index-und-geschützte-git-aktionen)
- [Decision Records](#decision-records)
- [Repository-Struktur](#repository-struktur)
- [Template- und abgeleitete Projektdateien](#template--und-abgeleitete-projektdateien)
- [Verwendung dieses Templates](#verwendung-dieses-templates)
- [Tool-Setup für Maintainer](#tool-setup-für-maintainer)
- [Kontinuierliche Verbesserung](#kontinuierliche-verbesserung)
- [Lizenz](#lizenz)

## Überblick

Das AGIT Documentation Template ist ein Ausgangspunkt für technische Dokumentationsprojekte, die expliziten Kontext, klare Zuständigkeiten, reproduzierbare Zusammenarbeit, dokumentierte Entscheidungen und prüfbare Publikations-Milestones benötigen. Es unterstützt Benutzer- und Administrationshandbücher, Tutorials, Betriebsanweisungen, Migrations- und Fehlerbehebungsleitfäden, technische Konzepte, Architekturdokumentation und gemischte Dokumentationswebsites.

Quarto Markdown ist das bevorzugte gepflegte Quellformat. Die Baseline rendert eine bilinguale HTML-Website und kann für DOCX- oder PDF-Review-Outputs angepasst werden. Links, Screenshots, Diagramme und erzeugte Outputs werden als Dokumentationsartefakte mit Provenienz, Sensitivitätsprüfung und Qualitätssicherung behandelt.

## Kernprinzip

Der Maintainer verantwortet Zweck, Umfang, Struktur, technische Korrektheit, Zielgruppenpassung und Veröffentlichungsentscheidungen der Dokumentation. Der Assistant kann beim Entwerfen, Umstrukturieren, Konsistenzprüfen, Planen von Visualisierungen und Prüfen von Outputs helfen, ersetzt aber weder das Maintainer-Urteil noch trifft er Veröffentlichungsentscheidungen.

Gepflegte Repository-Quellen sind maßgeblich. Gerenderte Websites, DOCX-Dateien, PDFs und annotierte Rückläufe sind Outputs oder Review-Artefakte, bis akzeptiertes Feedback in die Quelle zurückübertragen und dort validiert wurde.

## AGIT Templateverse

Die öffentlichen AGIT-Templates bilden ein kleines Templateverse: eine Familie verwandter Templates, die ein Repository-zentriertes, vom Maintainer geführtes Modell der Mensch-KI-Zusammenarbeit teilen und es für unterschiedliche Projekttypen spezialisieren.

- Das [AGIT Project Template](https://github.com/ctreffe/agit-project-template) ist der generische Ausgangspunkt für strukturierte Projektarbeit, Forschung, Planung, Konzeptarbeit, Prozessgestaltung und gemischte Projekte.
- Das [AGIT Dev Template](https://github.com/ctreffe/agit-dev-template) ist für entwicklungsorientierte Projekte gedacht, in denen Code, Skripte, Automatisierung, Validierung, Architektur oder Release-Workflows zentral sind.
- Das [AGIT Documentation Template](https://github.com/ctreffe/agit-docs-template) ist für technische Dokumentationsprojekte wie Benutzer- und Administrationshandbücher, Betriebsanweisungen, Tutorials, Migrationsleitfäden und Dokumentationswebsites gedacht.

## Wann dieses Template geeignet ist

Verwende dieses Template, wenn Zielgruppe, Struktur, Aufgabenführung, Links, Screenshots, visuelle QA und Publikationsformat von Beginn an zentral sind. Es ist besonders nützlich, wenn Dokumentation über Sprachen, Ausgabeformate oder Feedbackzyklen hinweg prüfbar bleiben muss.

Verwende das generische Project Template, wenn Dokumentation nur ein Teil eines breiteren Projekts ist. Verwende das Dev Template, wenn der Implementierungslebenszyklus primär ist und Dokumentation hauptsächlich Softwareverhalten begleitet.

## Projektinitialisierung

Die Initialisierung richtet das Dokumentationssystem ein, bevor umfangreiches Schreiben beginnt.

1. Erzeuge ein Repository aus diesem Template und lege die maßgebliche lokale Baseline fest.
2. Beginne mit [INITIAL_PROMPT.md](INITIAL_PROMPT.md) und folge [PROJECT_SETUP.md](PROJECT_SETUP.md).
3. Vervollständige [DOCS_SETUP.md](DOCS_SETUP.md) mit Dokumentationsidentität, Zweck, Umfang und Publikationsmodell.
4. Wähle das dominante Dokumentationstyp-Profil und mögliche sekundäre Profile.
5. Definiere primäre und sekundäre Zielgruppen, Vorwissen, Leseraufgaben und zu verhindernde Risiken in [AUDIENCE.md](AUDIENCE.md).
6. Entscheide, welche Sprachen veröffentlicht werden, ob eine maßgeblich ist und wie parallele Dokumente synchron bleiben.
7. Lege Regeln für Quellensensitivität, Screenshots, Links, Feedback und visuelle QA fest, bevor Rohmaterialien importiert werden.
8. Passe `_quarto.yml`, `docs/` und das projektspezifische Navigationsmodell an.
9. Vervollständige [PROJECT_CONTEXT.md](PROJECT_CONTEXT.md) mit Roadmap, aktueller Arbeit, Quellenmodell, Review-Modell und Template-Provenienz.
10. Rendere und prüfe die initiale Dokumentations-Baseline vor dem Initialisierungs-Commit.

Die Initialisierung ist unvollständig, solange erforderliche Entscheidungen zu Zweck, Zielgruppe, Struktur, Quellen, Veröffentlichung oder QA `TBD` bleiben.

## Empfohlene Workflows

### Dokumentationsworkflow

```text
Setup -> Struktur -> Quellen -> Entwurf -> Visualisierungen -> Review -> QA -> Milestone-Abschluss
```

Definiere Ausgangspunkt, Ziel und Voraussetzungen der Leser:innen, bevor eine Tutorial-Anleitung geschrieben wird. Entwirf in kleinen Abschnitten, validiere technische Wahrheit und Navigation, prüfe Links und Visualisierungen und halte aktuelle Dokumentation von historischer Erklärung getrennt.

Der vollständige laufende Prozess ist in [DOCUMENTATION_PROCESS.md](DOCUMENTATION_PROCESS.md) dokumentiert; Profile befinden sich in [DOCUMENTATION_TYPE_PROFILES.md](DOCUMENTATION_TYPE_PROFILES.md).

### Feedback-Workflows

Das Projekt unterstützt komplementäre Review-Kanäle:

1. **Direktes Quellenreview:** Maintainer bearbeiten oder kommentieren Quarto- oder Markdown-Quellen direkt.
2. **Maintainer-DOCX-Review:** Kommentare und Änderungsverfolgung werden in die gepflegte Quelle zurückübertragen, wenn ihre Intention eindeutig ist.
3. **Externes DOCX-Review:** Nicht kuratiertes externes Feedback wird als nummerierte Punkte dargestellt, bis der Maintainer es akzeptiert, ablehnt, qualifiziert oder zurückstellt.
4. **Annotiertes PDF-Review:** Layout-, Paginierungs-, Tabellen-, Abbildungs- und Druckprobleme werden auf ihre Quellstellen abgebildet und im gerenderten Format erneut validiert.
5. **Website-Review:** Jedes Artefakt benennt die abgedeckte Seite, das Kapitel, Bundle oder den Snapshot; ein mehrdeutiger Export gilt nicht als Review der gesamten Website.

Assistant-Zugriff, Git-Versionierung und Veröffentlichung von Review-Artefakten sind getrennte Entscheidungen. [FEEDBACK_WORKFLOW.md](FEEDBACK_WORKFLOW.md) beschreibt den vollständigen nachvollziehbaren Review-Zyklus.

## Git-Index und geschützte Git-Aktionen

Der Maintainer kontrolliert die Git-Historie. Assistants dürfen Status, Diffs und Logs prüfen, Dokumentationsänderungen vorbereiten sowie Commit-Grenzen und -Metadaten vorschlagen.

Staging und Unstaging sind Indexoperationen. Sie benötigen kein Kontrollwort, dürfen aber nur nach einer konkreten Maintainer-Anweisung oder Autorisierung des zugehörigen Commits erfolgen. Bestehende Staging-Auswahlen und nicht zusammenhängende Änderungen müssen erhalten bleiben.

Geschützte Aktionen umfassen Commits, Amendments, Tags, Pushes, Pulls, Merges, Rebases, Resets, Branch-Wechsel, Stash-Manipulationen und andere Operationen an der Git-Historie. Ein Assistant darf eine bestimmte geschützte Aktion nur ausführen, wenn die Anweisung für genau diese Aktion `explicit` oder `explicitly` auf Englisch oder die deutsche Wortfamilie `explizit` enthält. Die Freigabe von Dateiänderungen autorisiert keine Änderung der Git-Historie; die Freigabe einer geschützten Aktion autorisiert keine andere.

Reguläre Dokumentations-Commits verwenden normalerweise `docs:` oder ein anderes passendes Conventional-Commit-Präfix. Milestone-Commits verzichten auf das Präfix, enthalten die abgeschlossene Version und schließen Dokumentation ab, die bereits in regulären Schritten entworfen, geprüft und korrigiert wurde.

## Decision Records

Wähle den Record-Typ nach dem Entscheidungsgegenstand:

- **DDR — Documentation Decision Record:** Informationsarchitektur, Zielgruppenannahmen, Terminologie, bilinguales Modell, Screenshot-Richtlinien, Linkmodell, visuelle Standards, Publikationsworkflow oder Milestone-Umfang.
- **PDR — Project Decision Record:** Projektumfang, Roadmap, Zusammenarbeit, Datenschutz, Quellen-Governance oder Repository-Struktur.
- **ADR — Architecture Decision Record:** Quarto-Struktur, Build-Pipeline, Tooling, Output-Modell, Automatisierung oder eine andere dauerhafte Entscheidung zum technischen Dokumentationssystem.

Vorlagen befinden sich in [decisions/](decisions/). Erstelle einen Record nur, wenn Begründung und Konsequenzen für künftige Maintainer relevant bleiben; gewöhnliche Formulierungsänderungen und Routinekorrekturen benötigen keinen.

## Repository-Struktur

### Einstiegspunkte und Projektgedächtnis

- **`README.md` und `README.de.md`** erklären Template, initiales Setup und laufende Nutzung. Englisch ist maßgeblich, während Deutsch als enge Übersetzung gepflegt wird.
- **`PROJECT_CONTEXT.md`** hält Dokumentationszweck, Zielgruppe, Quellen- und Sensitivitätsmodell, aktuelle Arbeit, Roadmap, Review-Zustand und nächste Sitzung fest. Sie ist der primäre Wiedereinstiegspunkt und kein Ersatz für die Dokumentation selbst.
- **`CHANGELOG.md` und `VERSION`** dokumentieren abgeschlossene Template- oder Dokumentations-Milestones. Sie sollen einen geprüften Zustand abbilden und nicht Arbeit, die lediglich begonnen wurde.

### Zusammenarbeit, Setup und Prozess

- **`ChatGPT.md`** definiert Maintainer-Autorität, Repository-zentrierte Dokumentationsarbeit, Milestones, Feedback und Publikationsgrenzen.
- **`CODEX.md`** definiert lokalen Assistant-Zugriff, Behandlung sensibler Quellen, Rendering, Git und Übergaberegeln.
- **`PROJECT_SETUP.md`, `INITIAL_PROMPT.md` und `DOCS_SETUP.md`** legen Repository-Identität, Dokumentationstyp, Zielgruppe, Sprachen, Quellenmodell, Quarto-System und QA-Erwartungen fest. Die ersten beiden bleiben normalerweise als Initialisierungsprovenienz erhalten.
- **`CONTINUATION_PROMPT.md`** rekonstruiert Quellen-, Review-, QA- und Git-Baseline in einer späteren Sitzung.
- **`HARMONIZATION_PROMPT.md`** gleicht ein abgeleitetes Dokumentationsprojekt mit seiner aufgezeichneten Template-Baseline, internen Quellen, Outputs und Roadmap ab.
- **`RETROSPECTIVE_PROMPT.md`** bewertet Kollaborationspraktiken separat und kontrolliert, wie wiederverwendbare Erkenntnisse zu Template-Kandidaten werden.

### Dokumentationsregeln und Entscheidungen

- **`DOCUMENTATION.md` und `DOCUMENTATION_PROCESS.md`** definieren Dokumentrollen und den laufenden Weg von Setup über Entwurf, Review und QA bis zum Milestone-Abschluss.
- **`DOCUMENTATION_TYPE_PROFILES.md`** passt Struktur, Tiefe, Ton, Beispiele und Prüfungen an Tutorials, Guides, Referenzen, Konzepte und andere Dokumentationstypen an.
- **`AUDIENCE.md` und `STYLE_GUIDE.md`** machen Leserwissen, Aufgaben, Risiken, Terminologie und Schreiberwartungen explizit.
- **`LINKS.md`, `SCREENSHOTS.md` und `VISUAL_QA.md`** regeln Navigation, externe Nachweise, visuelle Erfassung, Sensitivität, Lesbarkeit und Publikationsreife.
- **`FEEDBACK_WORKFLOW.md`** definiert quellenmaßgebliche DOCX-, PDF- und Website-Review-Zyklen sowie den Umgang mit Maintainer- und externem Feedback.
- **`decisions/`** enthält DDR-, PDR- und ADR-Vorlagen sowie akzeptierte dauerhafte Entscheidungen in abgeleiteten Projekten.

### Quarto-Quellen, Assets und Review-Artefakte

- **`_quarto.yml`** definiert Dokumentationswebsite, Navigation, Output-Verzeichnis und Renderumfang. Abgeleitete Projekte passen Titel, Seiten, Sprachen und erforderliche Formate an.
- **`docs/`** enthält die gepflegten Quarto-Dokumentationsquellen einschließlich englischer und deutscher Einstiegsseiten in der Baseline. Diese Quellen sind gegenüber gerenderten Outputs maßgeblich.
- **`assets/`** enthält bewusst gepflegte Bilder, Diagramme und andere Publikationsassets. Jedes Artefakt soll einen klaren Zweck, Provenienz und Sensitivitätsstatus besitzen.
- **`review/`** dokumentiert lokale Review-Orte. Gerenderte und annotierte Artefakte werden standardmäßig ignoriert, weil Review-Zugriff, Git-Versionierung und Veröffentlichung getrennte Entscheidungen benötigen.

## Template- und abgeleitete Projektdateien

In einem abgeleiteten Dokumentationsprojekt:

- ersetze Platzhalter für Identität, Zielgruppe und Dokumentationsseiten durch konkrete Projektinhalte;
- vervollständige `DOCS_SETUP.md`, `AUDIENCE.md` und `PROJECT_CONTEXT.md`;
- passe `_quarto.yml`, `docs/`, Stil-, Link-, Screenshot- und visuelle QA-Leitlinien an;
- behalte `PROJECT_SETUP.md` und `INITIAL_PROMPT.md` als Initialisierungsprovenienz;
- behalte die Prompts für Fortsetzung, Harmonisierung und Retrospektive zur späteren Nutzung;
- pflege `DOCUMENTATION.md`, `REPOSITORY.md` und `FEEDBACK_WORKFLOW.md` als aktive Projektregeln;
- halte gerenderte und annotierte Artefakte standardmäßig lokal und versioniere sie erst nach bewusster Prüfung;
- erstelle echte Decision Records nur für dauerhafte Projekt-, Dokumentations- oder Architekturentscheidungen.

Halte initiale Template-Version und -Commit, letzte Harmonisierungs-Baseline, Lebenszyklusstatus und beabsichtigte Abweichungen in `PROJECT_CONTEXT.md` fest. Konkrete Zielgruppenentscheidungen und akzeptierte Decision Records bleiben gegenüber späteren generischen Template-Änderungen maßgeblich.

## Verwendung dieses Templates

1. Initialisiere das Repository mit `INITIAL_PROMPT.md`, `PROJECT_SETUP.md` und `DOCS_SETUP.md`.
2. Wähle das Dokumentationstyp-Profil und definiere Zielgruppen-, Sprach- und Publikationsanforderungen.
3. Lege Quelleninventar und Sensitivitätsgrenzen fest, bevor Screenshots, Logs, Exporte, Tickets oder Betriebsdaten geöffnet werden.
4. Definiere die Informationsarchitektur vor umfangreichem Entwurf.
5. Pflege Dokumentation in `docs/` und verbinde jede Visualisierung und jeden Link mit einer realen Leseraufgabe oder einem Nachweisbedarf.
6. Entwirf, rendere und prüfe in kleinen Schritten.
7. Übertrage akzeptiertes DOCX-, PDF- oder Website-Feedback zurück in die gepflegte Quelle und validiere es dort erneut.
8. Dokumentiere folgenreiche DDRs, PDRs oder ADRs in `decisions/`.
9. Halte `PROJECT_CONTEXT.md` aktuell und verwende `CONTINUATION_PROMPT.md` für spätere Sitzungen.
10. Schließe Milestones erst nach technischer, Zielgruppen-, Link-, visueller, Render- und Offenlegungs-QA ab.

## Tool-Setup für Maintainer

Für den Standard-Quarto-Workflow:

1. Installiere die [Quarto CLI](https://quarto.org/docs/get-started/) und prüfe sie mit `quarto --version`.
2. Öffne das Repository als aktiven lokalen Workspace und führe `quarto render` aus, um die HTML-Baseline zu validieren.
3. Installiere eine TeX-Toolchain wie TinyTeX nur, wenn direkter PDF-Output erforderlich ist.
4. Installiere LibreOffice, wenn DOCX-Outputs für visuelle QA in PDF oder Seitenbilder gerendert werden müssen.
5. Verwende R und RStudio nur, wenn die Dokumentation R-Code, Datenanalysen, Plots oder R-basierte Quarto-Erweiterungen enthält; für gewöhnliche Markdown-Dokumentation sind sie nicht erforderlich.

Halte erzeugte Websites, Previews, Rohcaptures und Review-Artefakte in den durch `.gitignore` definierten ignorierten Orten, sofern das Projekt nicht bewusst ein versioniertes Artefakt freigibt.

## Kontinuierliche Verbesserung

Nutze Harmonisierung, um ein abgeleitetes Dokumentationsprojekt mit relevanten Template-Entwicklungen, aktuellen Zielgruppenbedürfnissen, gepflegten Quellen, Outputs und Roadmap abzugleichen. Nutze Retrospektiven separat, um Zusammenarbeit, Übergaben und Review-Praktiken zu bewerten.

Wiederverwendbare Verbesserungen sollen in betroffene Leitlinien integriert statt als isolierte Notizen angehängt werden. Eine einzelne Projektbeobachtung ist nicht automatisch eine Template-Regel, und Publikationsentscheidungen verbleiben beim Maintainer.

## Lizenz

Dieses Template steht unter der [MIT-Lizenz](LICENSE).
