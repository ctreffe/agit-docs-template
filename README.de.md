# AGIT Documentation Template

[![Status](https://img.shields.io/badge/status-stable-green)](VERSION)
[![Version](https://img.shields.io/github/v/tag/ctreffe/agit-docs-template?label=version)](CHANGELOG.md)
[![License](https://img.shields.io/github/license/ctreffe/agit-docs-template)](LICENSE)

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

<br>

**[Link to the English README](README.md)**

<br>

## Inhalt

- [Überblick](#überblick)
- [Kernprinzip](#kernprinzip)
- [AGIT Templateverse](#agit-templateverse)
- [Wann dieses Template geeignet ist](#wann-dieses-template-geeignet-ist)
- [Projektinitialisierung](#projektinitialisierung)
- [Externe Dateien und Quellen](#externe-dateien-und-quellen)
- [Temporäre Arbeitsdateien](#temporäre-arbeitsdateien)
- [Projektmaterialien](#projektmaterialien)
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

Quarto Markdown ist das bevorzugte gepflegte Quellformat. Die Baseline rendert eine bilinguale HTML-Website und kann für DOCX- oder PDF-Review-Outputs angepasst werden. Links, Screenshots, Diagramme und erzeugte Outputs werden als Dokumentationsdateien mit Provenienz, Sensitivitätsprüfung und Qualitätssicherung behandelt.

## Kernprinzip

Der Maintainer verantwortet Zweck, Umfang, Struktur, technische Korrektheit, Zielgruppenpassung und Veröffentlichungsentscheidungen der Dokumentation. Der Assistant kann beim Entwerfen, Umstrukturieren, Konsistenzprüfen, Planen von Visualisierungen und Prüfen von Outputs helfen, ersetzt aber weder das Maintainer-Urteil noch trifft er Veröffentlichungsentscheidungen.

Gepflegte Repository-Quellen sind maßgeblich. Gerenderte Websites, DOCX-Dateien, PDFs und annotierte Rückläufe sind Outputs oder Review-Dateien, bis akzeptiertes Feedback in die Quelle zurückübertragen und dort validiert wurde.

## AGIT Templateverse

Die öffentlichen AGIT-Templates bilden ein kleines Templateverse: eine Familie verwandter Templates, die ein Repository-zentriertes, vom Maintainer geführtes Modell der Mensch-KI-Zusammenarbeit teilen und es für unterschiedliche Projekttypen spezialisieren.

- Das [AGIT Project Template](https://github.com/ctreffe/agit-project-template) ist der generische Ausgangspunkt für strukturierte Projektarbeit, Forschung, Planung, Konzeptarbeit, Prozessgestaltung und gemischte Projekte.
- Das [AGIT Dev Template](https://github.com/ctreffe/agit-dev-template) ist für entwicklungsorientierte Projekte gedacht, in denen Code, Skripte, Automatisierung, Validierung, Architektur oder Release-Workflows zentral sind.
- Das [AGIT Documentation Template](https://github.com/ctreffe/agit-docs-template) ist für technische Dokumentationsprojekte wie Benutzer- und Administrationshandbücher, Betriebsanweisungen, Tutorials, Migrationsleitfäden und Dokumentationswebsites gedacht.

## Wann dieses Template geeignet ist

Verwende dieses Template, wenn Zielgruppe, Struktur, Aufgabenführung, Links, Screenshots, visuelle QA und Publikationsformat von Beginn an zentral sind. Es ist besonders nützlich, wenn Dokumentation über Sprachen, Ausgabeformate oder Feedbackzyklen hinweg prüfbar bleiben muss.

Verwende das generische Project Template, wenn Dokumentation nur ein Teil eines breiteren Projekts ist. Verwende das Dev Template, wenn der Implementierungslebenszyklus primär ist und Dokumentation hauptsächlich Softwareverhalten begleitet.

## Projektinitialisierung

Nach dem Erzeugen des Repositorys muss der Maintainer nur [INITIAL_PROMPT.md](INITIAL_PROMPT.md) aufrufen. Der Agent liest das Repository und alle Setup-Leitlinien und führt anschließend durch die vollständige Dokumentationsinitialisierung. Der Maintainer muss `PROJECT_SETUP.md` oder `DOCS_SETUP.md` nicht selbst öffnen oder ausführen.

Die einfachste Anweisung an den Agenten lautet:

> Lies `INITIAL_PROMPT.md` vollständig und führe den darin enthaltenen Initialisierungs-Prompt aus.

Die Datei muss dafür nicht geöffnet und ihr Prompt nicht in die Unterhaltung kopiert werden.

Der Agent:

1. liest die Kollaborations-, Dokumentations-, Setup-, Repository- und Entscheidungsregeln;
2. prüft die Baseline, ohne die Git-Historie zu verändern;
3. legt kompakte Fragen zu Zweck, Umfang, Dokumentationstyp, Zielgruppen, Sprachen, Publikation und QA vor;
4. fragt Entscheidungen zu Quellensensitivität, Screenshots, Feedback und visueller Prüfung ab, bevor Rohmaterial importiert wird;
5. passt nach den Antworten `DOCS_SETUP.md`, `AUDIENCE.md`, README-Dateien, `_quarto.yml`, `docs/` und Navigation an;
6. dokumentiert Roadmap, Quellenmodell, Review-Modell und Template-Provenienz in `PROJECT_CONTEXT.md`;
7. rendert und prüft die initiale Dokumentations-Baseline; und
8. übergibt den initialisierten Stand mit Prüfergebnissen, offenen Entscheidungen und vorgeschlagenen Commit-Metadaten.

`PROJECT_SETUP.md` und `DOCS_SETUP.md` bleiben Checklisten des Agenten und dokumentieren die Methode der Initialisierung. `INITIAL_PROMPT.md` ist der einzige benutzerorientierte Einstiegspunkt, der sie aktiviert.

Soll ein Projekt lokal bleiben und keinen Remote erhalten, beginne in diesem
ausgecheckten Template mit [CREATE_LOCAL_PROJECT_PROMPT.md](CREATE_LOCAL_PROJECT_PROMPT.md).
Der Prompt prüft das Ziel, erzeugt einen unabhängigen lokalen Clone ohne Remote
und ruft anschließend `INITIAL_PROMPT.md` auf; er ist keine zweite Initialisierung.

## Externe Dateien und Quellen

Lege neu erhaltene Screenshots, Exporte, Logs, Tickets, Referenzdokumente und andere externe Dateien zunächst in `input/intake/` ab. Dokumentiere sichere Metadaten, Provenienz und Klassifizierung in `input/CATALOG.md`; verwende die ignorierte Datei `input/CATALOG.local.md`, wenn Dateinamen, Pfade oder Details selbst sensibel sind.

Katalogisiere unveränderte externe Dienste, Datensätze und URLs auch dann, wenn
ihre Inhalte außerhalb des Repositorys bleiben. Nutze stabile öffentliche URLs
direkt und löse logische private oder gerätespezifische Orte über die ignorierte
`input/PATHS.local.md` auf.

- **`input/intake/`** ist der ignorierte Eingangsbereich für noch nicht klassifizierte Dateien. Ihre bloße Anwesenheit erlaubt keinen Zugriff durch den Assistant.
- **`input/restricted/`** ist ignoriert und für Dateien bestimmt, die nur der Maintainer oder ausdrücklich freigegebene lokale Prüfungen lesen dürfen.
- **`input/local/`** ist ignoriert und enthält Dateien, die der Assistant lokal verarbeiten darf, die aber nicht in Git gelangen dürfen.
- **`input/versioned/`** enthält geprüfte externe Dateien, die versioniert werden dürfen.

Assistant-Zugriff, Git-Versionierung und Veröffentlichung sind getrennte Entscheidungen. Eine Verschiebung dokumentiert die Klassifizierung, erweitert aber keine Berechtigung. Wenn eine freigegebene Datei zu gepflegter Dokumentation, einem Publikationsasset oder einem Review-Input wird, verschiebe sie nach `docs/`, `assets/` oder `review/`, sofern dieser Ort ihre Rolle klarer ausdrückt, und bewahre die Provenienz im Katalog.

## Temporäre Arbeitsdateien

Verwende `temp/` für wegwerfbare Dokumentations-Zwischendateien. Alle Inhalte
außerhalb von `temp/restricted/` sind für den Assistant lesbar; dieses
Restricted-Verzeichnis darf weder aufgelistet noch gelesen werden. Sämtliche temporären Inhalte werden
ignoriert, dürfen niemals versioniert werden und werden nicht katalogisiert.
Überführe dauerhafte Dateien nach `materials/`, bevor sie später zu gepflegter
Dokumentation werden.

## Projektmaterialien

Dateien in `input/` bleiben inhaltlich unverändert. OCR-Text, zugeschnittene
oder annotierte Screenshots, konvertierte Referenzen und andere bearbeitete
Kopien sind neue Projektmaterialien. `materials/` bewahrt diese für den
Assistant lesbaren Arbeitsgrundlagen auf, bis sie verworfen oder bewusst in
gepflegte Dokumentation oder Publikations-Assets überführt werden.

Registriere jede dauerhafte Datei in `materials/CATALOG.md` mit Zweck,
Transformation und `Based on`-Provenienz. Nutze das ignorierte
`materials/local/` für **`local`**, `materials/versioned/` für **`versioned`**
und einen stabilen logischen Ort im Katalog für **`external`**. Löse externe
Orte je Rechner in der ignorierten `materials/PATHS.local.md` auf, ausgehend
von `materials/PATHS.local.example.md`.

Assistant-Zugriff autorisiert weder Git-Versionierung noch Veröffentlichung.
Prüfe Dateien und überführe sie nur dann nach `docs/` oder `assets/`, wenn sie
zu gepflegtem Dokumentationsinhalt werden; Review-Pakete, Caches und finale
Publikationsoutputs bleiben an ihren etablierten Orten.

Nicht die Erzeugungsweise, sondern die aktuelle Projektrolle bestimmt den
Ablageort. Bewahre eine erzeugte Datei in `materials/` auf, wenn sie als
dauerhafte Arbeits- oder Quelldatei in weitere Dokumentationsschritte eingeht.
Lege sie in `output/` oder am dokumentierten Publikationsort ab, wenn sie als
Projektergebnis zur Nutzung, Prüfung, Übergabe, Veröffentlichung oder
Auslieferung bestimmt ist. Wegwerfbare Erzeugungszwischenstände bleiben in
`temp/`; gepflegte `docs/`-Quellen und Publikations-`assets/` behalten ihre
maßgeblichen Orte.

## Render-Validierung und visuelle QA

Die routinemäßige Render- und Output-Validierung darf Quarto ausführen und das
erzeugte HTML technisch prüfen, ohne den Browser-Skill zu öffnen. Sie prüft je
nach Relevanz Build-Erfolg, Warnungen, erforderliche Dateien, HTML-Struktur,
Links, referenzierte Assets und offensichtlich nicht gerenderte Quellinhalte.
Das zählt nicht als visuelle QA.

Visuelle QA bedeutet, dass der Agent gerendertes HTML tatsächlich mit dem
Browser-Skill oder gerenderte PDF-/DOCX-Seitenbilder mit dem passenden visuellen
Werkzeug inspiziert. Der Agent führt sie ausschließlich vor einem
Milestone-Abschluss oder auf ausdrückliche Anforderung des Maintainers durch.
Visuelle oder Layoutänderungen allein lösen keine visuelle QA durch den Agenten
aus; der Maintainer übernimmt die visuelle Prüfung während der normalen Arbeit.
Wenn das benötigte Werkzeug oder der Output nicht verfügbar ist, meldet der
Agent, dass keine visuelle QA durchgeführt wurde.

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
4. **Annotiertes PDF-Review:** Layout-, Paginierungs-, Tabellen-, Abbildungs- und Druckprobleme werden auf ihre Quellstellen abgebildet; die geänderte Quelle wird gerendert und technisch validiert, während der Agent visuelle QA nur vor einem Milestone-Abschluss oder auf ausdrückliche Anforderung durchführt.
5. **Website-Review:** Jede Review-Datei benennt die abgedeckte Seite, das Kapitel, Bundle oder den Snapshot; ein mehrdeutiger Export gilt nicht als Review der gesamten Website.

Assistant-Zugriff, Git-Versionierung und Veröffentlichung von Review-Dateien sind getrennte Entscheidungen. [FEEDBACK_WORKFLOW.md](FEEDBACK_WORKFLOW.md) beschreibt den vollständigen nachvollziehbaren Review-Zyklus.

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

- **`README.md` und `README.de.md`** erklären Template, initiales Setup und laufende Nutzung auf Englisch und Deutsch.
- **`PROJECT_CONTEXT.md`** hält Dokumentationszweck, Zielgruppe, Quellen- und Sensitivitätsmodell, aktuelle Arbeit, Roadmap, Review-Zustand und nächste Sitzung fest. Sie ist der primäre Wiedereinstiegspunkt und kein Ersatz für die Dokumentation selbst.
- **`CHANGELOG.md` und `VERSION`** dokumentieren abgeschlossene Template- oder Dokumentations-Milestones. Sie sollen einen geprüften Zustand abbilden und nicht Arbeit, die lediglich begonnen wurde.

### Zusammenarbeit, Setup und Prozess

- **`AGENTS.md`** ist der kompakte, automatisch geladene Einstiegspunkt für KI-Agenten. Die Datei führt zu den vollständigen Dokumentations-, Quellenschutz- und Validierungsleitlinien, ohne sie zu duplizieren.
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

### Quarto-Quellen, Assets und Review-Dateien

- **`_quarto.yml`** definiert Dokumentationswebsite, Navigation, Output-Verzeichnis und Renderumfang. Abgeleitete Projekte passen Titel, Seiten, Sprachen und erforderliche Formate an.
- **`docs/`** enthält die gepflegten Quarto-Dokumentationsquellen einschließlich englischer und deutscher Einstiegsseiten in der Baseline. Diese Quellen sind gegenüber gerenderten Outputs maßgeblich.
- **`input/`** klassifiziert eingehende externe Dateien und dokumentiert ihre Provenienz, bevor sie in gepflegte Dokumentationsworkflows gelangen.
- **`materials/`** katalogisiert dauerhafte, für den Assistant lesbare
  Dokumentations-Arbeitsdateien in lokaler, versionierter oder externer
  Speicherung.
- **`temp/`** enthält ignorierte, niemals versionierte
  Dokumentations-Zwischenstände; `temp/restricted/` bildet die nicht
  zugängliche Ausnahme.
- **`assets/`** enthält bewusst gepflegte Bilder, Diagramme und andere Publikationsdateien. Jede Datei soll einen klaren Zweck, Provenienz und Sensitivitätsstatus besitzen.
- **`review/`** dokumentiert lokale Review-Orte. Gerenderte und annotierte Review-Dateien werden standardmäßig ignoriert, weil Review-Zugriff, Git-Versionierung und Veröffentlichung getrennte Entscheidungen benötigen.

## Template- und abgeleitete Projektdateien

In einem abgeleiteten Dokumentationsprojekt:

- ersetze Platzhalter für Identität, Zielgruppe und Dokumentationsseiten durch konkrete Projektinhalte;
- behalte `AGENTS.md` als automatischen Agenten-Einstiegspunkt und passe die Datei an;
- vervollständige `DOCS_SETUP.md`, `AUDIENCE.md` und `PROJECT_CONTEXT.md`;
- passe `_quarto.yml`, `docs/`, Stil-, Link-, Screenshot- und visuelle QA-Leitlinien an;
- behalte `PROJECT_SETUP.md` und `INITIAL_PROMPT.md` als Initialisierungsprovenienz;
- behalte die Prompts für Fortsetzung, Harmonisierung und Retrospektive zur späteren Nutzung;
- pflege `DOCUMENTATION.md`, `REPOSITORY.md` und `FEEDBACK_WORKFLOW.md` als aktive Projektregeln;
- halte gerenderte und annotierte Review-Dateien standardmäßig lokal und versioniere sie erst nach bewusster Prüfung;
- erstelle echte Decision Records nur für dauerhafte Projekt-, Dokumentations- oder Architekturentscheidungen.

Halte initiale Template-Version und -Commit, letzte Harmonisierungs-Baseline, Lebenszyklusstatus und beabsichtigte Abweichungen in `PROJECT_CONTEXT.md` fest. Konkrete Zielgruppenentscheidungen und akzeptierte Decision Records bleiben gegenüber späteren generischen Template-Änderungen maßgeblich.

## Verwendung dieses Templates

1. Erzeuge ein Repository aus dem Template und gib dem Agenten die Anweisung aus `INITIAL_PROMPT.md`.
2. Beantworte die nummerierten Fragen des Agenten; er liest und verarbeitet `PROJECT_SETUP.md`, `DOCS_SETUP.md` und die übrigen Setup-Leitlinien automatisch.
3. Prüfe den initialisierten Dokumentationsstand, die Render-Prüfungen und den vorgeschlagenen ersten Commit.
4. Wähle das Dokumentationstyp-Profil und bestätige mit dem Agenten Zielgruppen-, Sprach- und Publikationsanforderungen.
5. Lege Quelleninventar und Sensitivitätsgrenzen fest, bevor Screenshots, Logs, Exporte, Tickets oder Betriebsdaten geöffnet werden.
6. Definiere die Informationsarchitektur vor umfangreichem Entwurf und entwirf, rendere und prüfe anschließend in kleinen Schritten.
7. Verbinde jede Visualisierung und jeden Link mit einer realen Leseraufgabe oder einem Nachweisbedarf.
8. Übertrage akzeptiertes Feedback zurück in die gepflegte Quelle und validiere es dort erneut.
9. Dokumentiere folgenreiche Entscheidungen, halte `PROJECT_CONTEXT.md` aktuell und verwende `CONTINUATION_PROMPT.md` für spätere Sitzungen.
10. Schließe Milestones erst nach technischer, Zielgruppen-, Link-, visueller, Render- und Offenlegungs-QA ab.

## Tool-Setup für Maintainer

Für den Standard-Quarto-Workflow:

1. Installiere die [Quarto CLI](https://quarto.org/docs/get-started/) und prüfe sie mit `quarto --version`.
2. Öffne das Repository als aktiven lokalen Workspace und führe `quarto render` aus, um die HTML-Baseline zu validieren.
3. Folge Quartos [Hinweisen zu TinyTeX und PDF-Engines](https://quarto.org/docs/output-formats/pdf-engine) nur, wenn direkter PDF-Output erforderlich ist.
4. Installiere [LibreOffice](https://www.libreoffice.org/download/instructions/), wenn DOCX-Outputs für visuelle QA in PDF oder Seitenbilder gerendert werden müssen.
5. Verwende [R](https://cran.r-project.org/) und [RStudio](https://posit.co/downloads/) nur, wenn die Dokumentation R-Code, Datenanalysen, Plots oder R-basierte Quarto-Erweiterungen enthält; für gewöhnliche Markdown-Dokumentation sind sie nicht erforderlich.

Halte erzeugte Websites, Previews, ungeprüfte Captures und Review-Dateien in den durch `.gitignore` definierten ignorierten Orten, sofern das Projekt nicht bewusst eine versionierte Datei oder einen versionierten Output freigibt.

## Kontinuierliche Verbesserung

Nutze Harmonisierung, um ein abgeleitetes Dokumentationsprojekt mit relevanten Template-Entwicklungen, aktuellen Zielgruppenbedürfnissen, gepflegten Quellen, Outputs und Roadmap abzugleichen. Nutze Retrospektiven separat, um Zusammenarbeit, Übergaben und Review-Praktiken zu bewerten.

Behandle Feedback-Muster, Navigationsprobleme, Renderfehler, Visual-QA-Befunde und Publikationserfahrungen als Evidenz für mögliche Verbesserungen. Eine einzelne Projektbeobachtung ist nicht automatisch eine Template-Regel; prüfe Zielgruppe, Dokumentationstyp, Ausgabeformat und Wartungskosten, bevor Du sie verallgemeinerst.

Der Maintainer koordiniert die templateübergreifende Weiterentwicklung in einem privaten Governance-Repository namens `agit-templateverse`. Es dokumentiert gemeinsame Konventionen, bewusste Spezialisierungen und Evidenz aus abgeleiteten Projekten. Das Repository wird bewusst nicht verlinkt, da Template-Nutzer:innen keinen Zugriff darauf benötigen.

Die Governance-Koordination erzeugt keine verborgenen Dokumentationsanforderungen. Jede Änderung, die dieses Template betrifft, muss hier durch gepflegte Leitlinien, gegebenenfalls Documentation Decision Records, den Changelog und die Release-Historie abgebildet werden. Wiederverwendbare Verbesserungen sollen in betroffene Quellen-, Feedback-, Render- und QA-Leitlinien integriert werden; Publikationsentscheidungen verbleiben beim Maintainer.

## Lizenz

Dieses Template steht unter der [MIT-Lizenz](LICENSE).
