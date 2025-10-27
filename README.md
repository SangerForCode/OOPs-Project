# Food Ordering System — Sales Analytics & Backend Management (FK / INS)

Author: Ayush Sanger  
ID: 2023B2AD0742G

## Project overview

At BITS Goa the food outlets INS and FK experience long queues, order mistakes, and slow cash handling. This project implements the Sales Analytics & Backend Management module for a digital food-ordering ecosystem. The module centralizes online and offline (cash) transactions, runs ETL and analytics pipelines, updates a live sales dashboard, and automates PDF report generation (daily/monthly). The goal is to give outlet managers real-time visibility into sales, trends, and inventory signals so they can act quickly (menu changes, reorders, staffing adjustments).

Key capabilities:
- Collect and unify order data (online + offline)
- ETL and trend/forecast analysis
- Anomaly detection for suspicious or incorrect entries
- Live dashboard APIs for managers and admins
- Automated PDF report generation and scheduled emailing
- Inventory tracking and reorder suggestions

## Files added

The following diagram source files have been added under `diagrams/`. These are the editable sources (PlantUML / Mermaid) so you can render or edit them locally and push to GitHub.

- `diagrams/state_chart.puml` — PlantUML source for the Sales Analytics state chart (data collection → analytics → reporting → manager actions).
- `diagrams/use_case.puml` — PlantUML source for the Use-Case diagram showing actors and use cases (collect, dashboard, reports, analytics, integrations).
- `diagrams/class_diagram.mmd` — Mermaid class diagram (core ordering classes, analytics, relationships).
- `diagrams/class_diagram_abstract.mmd` — Mermaid class diagram (abstract Order and Comparable interface variant).
- `diagrams/gantt.mmd` — Mermaid Gantt chart for the project timeline and milestones.

## How to render these diagrams

Mermaid
- GitHub supports Mermaid inside Markdown (fenced code blocks) in some views; however, `.mmd` files may not render automatically in the file preview. To preview locally, use a VS Code extension such as "Markdown Preview Enhanced" or "vscode-mermaid-preview". You can also copy the Mermaid block into a `.md` file inside a fenced ```mermaid block and GitHub will render it where supported.

PlantUML
- To render the PlantUML `.puml` files locally you can either:
	- Install the VS Code "PlantUML" extension (recommended) and preview diagrams directly.
	- Use the PlantUML jar to generate images:

```bash
# Download plantuml.jar once (example):
wget -O plantuml.jar https://github.com/plantuml/plantuml/releases/latest/download/plantuml.jar

# Generate PNGs from the `diagrams` folder:
java -jar plantuml.jar diagrams/*.puml
```

Or run PlantUML via Docker:

```bash
docker run --rm -v "$(pwd)":/workspace plantuml/plantuml:latest diagrams/state_chart.puml
```

## How to upload to GitHub and link to your submission

1. Create a GitHub repository (on the GitHub website). Note the repository URL (e.g. `https://github.com/YOUR_USERNAME/YOUR_REPO`).
2. From your local project directory, run:

```bash
git init
git add .
git commit -m "Add diagrams and project README — Sales Analytics & Backend Management"
git branch -M main
git remote add origin https://github.com/YOUR_USERNAME/YOUR_REPO.git
git push -u origin main
```

3. Copy the repo URL (or GitHub Pages link if you enable Pages) and paste it into your official submission page as required by your course. Example URL to paste as a submission:

`https://github.com/YOUR_USERNAME/YOUR_REPO`

Replace `YOUR_USERNAME` and `YOUR_REPO` with your GitHub username and repository name.

## Notes & next steps

- If you want the diagrams to render directly on the GitHub repository root README, consider embedding Mermaid blocks inside `README.md` or adding generated PNG/SVG outputs to the repo (e.g., `diagrams/*.png`) committed alongside the sources.
- If you want, I can also generate PNG/SVG from the PlantUML files here and commit them to `diagrams/` so the visuals show on GitHub without extra setup; tell me which formats you prefer (PNG or SVG).

## Contact / Submission

If you need the final GitHub URL added to your official submission page, provide the submission portal link (or tell me where to add it) and I can prepare a short submission note (with the repo link and summary) that you can paste into the portal.

---
Generated and organized diagram sources are in `diagrams/`. Next: I will commit the README and optionally generate rendered images if you want them included for direct GitHub viewing.

