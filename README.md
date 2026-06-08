# Inside LLMs

A lightweight Marp workshop deck that explains how LLMs work, from tokenization through transformers and next-token generation.

The source deck is authored in Markdown, images live in `Resources/`, and the build scripts generate a static site for local preview or GitHub Pages deployment.

## Repository Structure

```text
.
|-- README.md
|-- package.json
|-- package-lock.json
|-- Resources/
|   |-- Basics_Slide_01.png
|   |-- Intermediate_Slide_01.png
|   |-- Slide_0.png
|   |-- ...
|-- decks/
|   `-- owasp-top10-llm/
|       |-- deck.yml
|       `-- slides.md
|-- scripts/
|   |-- build-deck.js
|   `-- build-site.js
`-- .github/
    `-- workflows/
        `-- pages.yml
```

## Prerequisites

- Node.js 20+
- npm

## Quick Start

```bash
npm install
npm run build
npm run preview
```

Open the local URL printed by the preview command.

## Available Commands

| Command | What it does |
| --- | --- |
| `npm install` | Installs Marp CLI and the local preview server. |
| `npm run build` | Builds the complete static site into `site/`. |
| `npm run site` | Alias for the complete site build. |
| `npm run build:deck` | Builds only the slide deck HTML into `site/owasp-top10-llm/`. |
| `npm run preview` | Serves the generated `site/` directory locally with caching disabled. |

## Editing the Slide Deck

- Edit `decks/owasp-top10-llm/slides.md`.
- Slides are separated with `---`.
- Add images to `Resources/` and reference them from the deck.
- Rebuild after making changes.

Example slide:

```markdown
---

## New Slide Title

Your content here.
```

Example full-slide image:

```markdown
---

<!-- _class: image -->
![bg contain](../../Resources/my-new-slide.png)
```

## Editing Deck Metadata

- Edit `decks/owasp-top10-llm/deck.yml`.
- `slug` controls the deck path under `site/`.

Example:

```yaml
slug: owasp-top10-llm
title: AI Security Learning Notes
subtitle: OWASP Top 10 LLM Workshop
description: Slide deck for AI security concepts.
tags:
  - ai-security
  - llm
  - owasp
  - workshop
```

## Generated Output

```text
site/
|-- index.html
|-- Resources/
|   |-- copied image assets
`-- owasp-top10-llm/
    `-- index.html
```

Do not edit files in `site/` manually. They are regenerated on each build.

## Deploying to GitHub Pages

- Workflow file: `.github/workflows/pages.yml`
- Trigger: push to `main` or manual `workflow_dispatch`
- Build command used by CI: `npm run site`

To use this deployment flow, set Pages source to GitHub Actions in repository settings.

## Troubleshooting

### Marp CLI not installed

```bash
npm install
```

### Images are missing

- Confirm the file exists in `Resources/`.
- Confirm spelling/case matches exactly.
- Confirm the deck reference starts with `../../Resources/`.
- Rebuild with `npm run build`.

### `site/` is missing

```bash
npm run build
```

## Contribution Flow

1. Edit `decks/owasp-top10-llm/slides.md`, `decks/owasp-top10-llm/deck.yml`, or `Resources/`.
2. Run `npm run build`.
3. Run `npm run preview`.
4. Review the deck in a browser.
5. Commit the source changes.
6. Push to `main` when ready to deploy.

Generated output in `site/` should usually not be edited or committed unless your workflow explicitly requires it.

## Attribution

The OWASP Top 10 for LLM Applications 2025 training content in this repository was designed and developed by CN Madhu. The program combines industry-relevant content and practical labs to showcase real-world AI security risks, vulnerabilities, and defense strategies in healthcare environments.

## License

No explicit license file is currently included. Confirm usage rights with the repository owner before redistributing or reusing this material.
