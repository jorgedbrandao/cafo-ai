# Cafo Commercial Architecture

This directory houses the intelligence, playbooks, tools, and memory for the Cafo commercial team. It is designed to act as a comprehensive system for training, execution, and continuous improvement in sales.

## Architecture Components

The architecture is divided into four main pillars: Skills, Playbooks, Tools, and Memory.

### 1. Skills (The Agents)
These are the specialized personas that define our sales methodology. They exist as markdown files in this root directory.
*   **Deal Strategist:** (`sales-deal-strategist.md`) Focuses on MEDDPICC, risk assessment, and competitive positioning.
*   **Discovery Coach:** (`sales-discovery-coach.md`) Focuses on SPIN/Gap selling, asking the right questions, and uncovering root pain.
*   **Outbound Strategist:** (`sales-outbound-strategist.md`) Focuses on signal-based selling, sequence architecture, and cold outreach.
*   **Account Strategist:** (`sales-account-strategist.md`) Focuses on land-and-expand, QBRs, and net revenue retention (NRR).
*   **Sales Engineer:** (`sales-engineer.md`) Focuses on technical discovery, POC scoping, and demo engineering.
*   **Sales Coach:** (`sales-coach.md`) Focuses on rep development, call coaching, and forecast accuracy.
*   **Proposal Strategist:** (`sales-proposal-strategist.md`) Focuses on win themes and compelling proposal narratives.
*   **Pipeline Analyst:** (`sales-pipeline-analyst.md`) Focuses on pipeline velocity, health diagnostics, and forecasting.

### 2. Playbooks (`/playbooks` directory & `playbooks.md`)
The `playbooks.md` file defines the **Playbook Architect** skill, responsible for synthesizing the knowledge from the other skills into actionable, visually appealing (HTML/Markdown) guides for specific sales scenarios.
*   Generated playbooks are saved in the `playbooks/` subdirectory.
*   File naming convention: `YYYY-MM-DD_playbook_name.md`.

### 3. Tools (`tools.md`)
The `tools.md` file contains the **Tools Master** documentation. It provides the standardized Cafo design system (colors, typography) and HTML/CSS component snippets necessary to build beautiful, on-brand playbooks and proposals.

### 4. Memory (`commercial_memory.md`)
The `commercial_memory.md` file is the contextual log. It tracks *when* and *why* playbooks are created. This ensures the system understands the business context of each asset and knows when to trigger or update them in the future.

## Workflow Example
1.  **Trigger:** A new market segment is identified (e.g., small specialty coffee shops).
2.  **Skill Utilization:** The *Outbound Strategist* defines the signals, the *Discovery Coach* defines the SPIN questions, and the *Deal Strategist* defines the likely objections.
3.  **Playbook Creation:** The *Playbook Architect* uses the components from *Tools* to create `2026-05-02_specialty_coffee_pitch.md` in the `playbooks/` folder.
4.  **Memory Logging:** The creation event, persona, and key objections are logged in `commercial_memory.md`.
