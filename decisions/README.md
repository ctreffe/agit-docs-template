# Decision Records

This directory is the default location for durable decision records in documentation projects.

Use the record type that matches the decision:

- `DDR` - Documentation Decision Record for documentation structure, audience assumptions, terminology, screenshot policy, link model, visual standards, publication workflow or documentation milestone scope.
- `PDR` - Project Decision Record for scope, roadmap, collaboration, privacy, repository structure, governance or project-boundary decisions.
- `ADR` - Architecture Decision Record for Quarto structure, build pipeline, tooling, output model, automation or other technical documentation-system decisions.

Documentation projects usually use DDRs, but they may legitimately contain PDRs and ADRs as well. Choose the prefix by decision subject, not by repository type.

Use a DDR when a decision affects:

- Documentation structure or navigation.
- Audience assumptions.
- Terminology.
- Screenshot or visual-file policy.
- Link and source model.
- Publication workflow.
- Versioning or milestone scope.
- Handling of sensitive documentation material.

Decision records should be concise. They preserve why a decision was made, not every discussion that led to it.

## Naming

Use a stable prefix, number and short kebab-case title:

```text
DDR-0001-short-title.md
PDR-0001-project-scope.md
ADR-0001-quarto-output-model.md
```

## Templates

Use the matching template as a starting point:

- [DDR-0000-template.md](DDR-0000-template.md)
- [PDR-0000-template.md](PDR-0000-template.md)
- [ADR-0000-template.md](ADR-0000-template.md)
