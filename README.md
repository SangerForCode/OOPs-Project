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
