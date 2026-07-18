# AGIT Documentation Template

> [!NOTE]
> **AI Collaboration**
>
> Dieses Repository pflegt das AGIT Documentation Template.
>
> Das AGIT Documentation Template ist die dokumentationsorientierte Spezialisierung der AGIT Template-Familie.
>
> Das Collaboration Model dokumentiert Dokumentationspraktiken, KI-gestützte Dokumentationsworkflows, Link- und Visual-QA-Disziplin und Repository-Konventionen für Dokumentationsprojekte.
>
> Das Collaboration Model wird in [ChatGPT.md](ChatGPT.md) gepflegt.

Template für AI-gestützte technische Dokumentation in AGIT-Kontexten, mit repository-basiertem Workflow, Link-Disziplin, Screenshots, visueller Qualitätsprüfung und dokumentierten Entscheidungen.

Dieses Repository ist ein Ausgangspunkt für technische Dokumentationsprojekte, die mit ähnlicher Sorgfalt gepflegt werden sollen wie Software- und wissenschaftliche Schreibprojekte: expliziter Kontext, klare Verantwortung, reproduzierbare Zusammenarbeit, dokumentierte Entscheidungen und nachvollziehbare Meilensteine.

Englisches README: [README.md](README.md)

## Grundprinzip

Der Maintainer verantwortet jederzeit Dokumentationsziel, Struktur, technische Korrektheit, Zielgruppenpassung und finale Veröffentlichungsentscheidung. Der AI Assistant unterstützt beim Formulieren, bei Konsistenzprüfungen, Link-Disziplin, Screenshot- und Visual-QA, strukturellem Feedback und Repository-Pflege, ersetzt aber nicht die Maintainer-Entscheidung.

## Wofür dieses Template gedacht ist

Das Template eignet sich für Dokumentationsprojekte wie:

- Benutzerhandbücher, Admin-Guides und Betriebsanweisungen.
- Technische Konzepte, Architekturhinweise und Implementierungsdokumentation.
- Troubleshooting-, Migrations-, Setup- und Release-Dokumentation.
- Dokumentationssysteme mit Text, Screenshots, Diagrammen, Links und generierten Outputs.

## AGIT Templateverse

Die öffentlichen AGIT Templates bilden ein kleines Templateverse: eine Familie zusammenhängender Templates, die ein repository-first, maintainer-geführtes Modell für Human-AI Collaboration teilen und für unterschiedliche Projekttypen spezialisieren.

- [AGIT Project Template](https://github.com/ctreffe/agit-project-template) ist der generische Startpunkt für strukturierte Projektarbeit, Recherche, Planung, Konzeptarbeit, Prozessgestaltung und gemischte Projekte.
- [AGIT Dev Template](https://github.com/ctreffe/agit-dev-template) ist für entwicklungsorientierte Projekte gedacht, in denen Code, Skripte, Automatisierung, Validierung, Architektur oder Release-Workflows zentral sind.
- [AGIT Documentation Template](https://github.com/ctreffe/agit-docs-template) ist für technische Dokumentationsprojekte gedacht, etwa Benutzerhandbücher, Admin-Guides, Betriebsanweisungen, Tutorials, Migrationsguides und Dokumentationssites.

Das Documentation Template passt, wenn Zielgruppe, Struktur, Screenshots, Links, Visual QA und Publikationsformat von Anfang an zentral sind. Das generische Project Template passt, wenn Dokumentation nur ein Teil eines breiteren Projekts ist.

## Workflow

1. Mit [INITIAL_PROMPT.md](INITIAL_PROMPT.md) starten.
2. [PROJECT_SETUP.md](PROJECT_SETUP.md) und [DOCS_SETUP.md](DOCS_SETUP.md) ausfüllen.
3. Projektspezifischen Kontext in [PROJECT_CONTEXT.md](PROJECT_CONTEXT.md) festhalten.
4. Dokumentationstyp, Zielgruppe, Zweisprachigkeit, Quarto-Struktur, Links, Screenshots und Visual-QA festlegen.
5. Dokumentation in kleinen, prüfbaren Schritten erarbeiten.
6. Wichtige Entscheidungen in `decisions/` festhalten, normalerweise als DDRs.
7. Sinnvolle Meilensteine mit Changelog, Version und Konsistenzprüfung abschließen.
8. Spätere Kontextfenster oder Assistant-Sessions mit [CONTINUATION_PROMPT.md](CONTINUATION_PROMPT.md) beginnen.

## Kontrollwörter für Git-History-Aktionen

AI Assistants dürfen Git-History-Aktionen wie Staging, Commit, Tag, Push, Pull, Merge, Rebase, Reset oder Branch-Wechsel nur ausführen, wenn die Maintainer-Anweisung für genau diese Aktion ein anerkanntes Kontrollwort enthält.

Anerkannte Kontrollwörter sind `explicit` und `explicitly` in englischsprachigen Anweisungen sowie die deutsche Wortfamilie `explizit`, einschließlich gebeugter Formen wie `explizite`, `expliziten`, `expliziter` und `explizites`, in deutschsprachigen Anweisungen. Anfragen ohne eines dieser Kontrollwörter erlauben nur Vorbereitung und Anleitung.

## Maintainer-Setup

Für ein neues Codex-basiertes Dokumentationsprojekt empfiehlt sich diese Reihenfolge:

1. Neues Repository aus diesem Template erzeugen und lokal klonen.
2. Das Repository als aktiven Codex-Workspace öffnen.
3. Quarto CLI von <https://quarto.org/docs/get-started/> installieren.
4. Neues Terminal öffnen und Quarto mit `quarto --version` prüfen.
5. Falls PDF-Output benötigt wird, eine TeX-Toolchain installieren, zum Beispiel mit `quarto install tinytex`.
6. Quarto-Baseline mit `quarto render` prüfen.
7. Projektinitialisierung mit [INITIAL_PROMPT.md](INITIAL_PROMPT.md) starten.
8. [PROJECT_SETUP.md](PROJECT_SETUP.md), [DOCS_SETUP.md](DOCS_SETUP.md) und [PROJECT_CONTEXT.md](PROJECT_CONTEXT.md) ausfüllen.

R und RStudio sind sinnvoll, wenn die Dokumentation R-Code, Datenanalysen, Plots oder R-basierte Quarto-Erweiterungen enthält. Für einfache Markdown-basierte Dokumentation sind sie nicht zwingend erforderlich.

## Zentrale Dateien

- [ChatGPT.md](ChatGPT.md): Versioniertes AI Collaboration Model.
- [CODEX.md](CODEX.md): Lokale Arbeitsregeln für den Assistant.
- [DOCUMENTATION.md](DOCUMENTATION.md): Dokumentationsarchitektur und Rollen der Dateien.
- [PROJECT_SETUP.md](PROJECT_SETUP.md): Initialisierung abgeleiteter Projekte.
- [INITIAL_PROMPT.md](INITIAL_PROMPT.md): Erster Prompt für die Projektinitialisierung.
- [CONTINUATION_PROMPT.md](CONTINUATION_PROMPT.md): Wiedereinstiegsprompt für ein neues Kontextfenster oder eine neue Assistant-Session.
- [DOCS_SETUP.md](DOCS_SETUP.md): Dokumentationsspezifische Setup-Checkliste.
- [DOCUMENTATION_PROCESS.md](DOCUMENTATION_PROCESS.md): Laufender Dokumentationsprozess.
- [DOCUMENTATION_TYPE_PROFILES.md](DOCUMENTATION_TYPE_PROFILES.md): Dokumentationstyp-Profile, einschließlich Tutorial-Profil.
- [QUARTO.md](QUARTO.md): Quarto als bevorzugtes internes Dokumentationsformat.
- [AUDIENCE.md](AUDIENCE.md): Vorlage für das Zielgruppenmodell.
- [STYLE_GUIDE.md](STYLE_GUIDE.md): Stilprinzipien technischer Dokumentation.
- [SCREENSHOTS.md](SCREENSHOTS.md): Regeln für Screenshots und visuelle Belege.
- [LINKS.md](LINKS.md): Link- und Referenzdisziplin.
- [VISUAL_QA.md](VISUAL_QA.md): Checkliste für visuelle Qualitätsprüfung.
- [decisions/](decisions/): Decision Records, einschließlich DDRs, PDRs und ADRs.

## Lizenz

Dieses Template steht unter der MIT License. Siehe [LICENSE](LICENSE).
