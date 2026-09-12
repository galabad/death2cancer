# Breast Cancer Metabolism Research

An open, research-only multi-agent workflow for forming auditable hypotheses about whether medicines on the WHO Model List of Essential Medicines might affect metabolic pathways relevant to breast cancer.

This project is designed for the **Ambiguous** workspace: its wiki, forms, tasks, evidence inbox, and decision log provide shared context and an audit trail. Codex currently serves as the external execution layer while a native coworker runtime is unavailable.

## Public entry points

- [Project landing wiki](https://app.ambiguous.ai/wiki/breast-cancer-metabolism-research-public/breast-cancer-metabolism-research)
- [Request an evidence brief page](https://app.ambiguous.ai/wiki/breast-cancer-metabolism-research-public/request-breast-cancer-metabolism-evidence-brief)
- [Evidence-brief request form](https://app.ambiguous.ai/f/death2cancer/request-breast-cancer-metabolism-evidence-brief)
- [Published evidence briefs](https://app.ambiguous.ai/wiki/breast-cancer-metabolism-research-public/published-evidence-briefs)

The landing page also lists completed questions with direct brief links. Current examples:

- [What is the top drug for affecting breast-cancer metabolism?](https://app.ambiguous.ai/wiki/breast-cancer-metabolism-research/evidence-brief-leading-drug-candidates-breast-cancer-metabolism)
- [What drugs most affect hormones related to breast cancer?](https://app.ambiguous.ai/wiki/breast-cancer-metabolism-research/evidence-brief-breast-cancer-hormone-biology)

These are research-only evidence maps, not treatment recommendations.

## Four roles

1. **Metabolism Software & Model Analyst** — reproducible pathway, genome-scale metabolic-model, and chemoinformatics workflows.
2. **Tumour-Normal Data Steward** — lawful, documented access to cohort-level tumour and matched-normal resources.
3. **Essential-Medicines Chemoinformatics Analyst** — WHO medicine identifiers, chemistry, pharmacology, metabolism, and interaction evidence.
4. **Breast Metabolism Literature Evidence Curator** — literature identity, source status, evidence classification, and correction/retraction checks.

The Orchestrator triangulates: `medicine → target/mechanism → metabolic pathway → tumour evidence → normal-tissue context`.

## What this is—and is not

This is a transparent **hypothesis-generation and evidence-mapping** system. It is not medical advice, clinical decision support, dosing guidance, or a basis for patient-specific conclusions. Candidate findings require expert review by appropriate oncology, pharmacology, and molecular-tumour-board professionals.

## Repository guide

- [Architecture](docs/architecture.md)
- [Ambiguous setup](docs/ambiguous-setup.md)
- [Public request workflow](docs/public-request-workflow.md)
- [Research governance](docs/research-governance.md)
- [Data and privacy policy](docs/data-and-privacy.md)
- [Contribution guide](CONTRIBUTING.md)

## Quick start

1. Create an Ambiguous workspace and configure an agent credential locally; never commit credentials.
2. Create a research wiki space, the four role pages, an Evidence Inbox, Candidate Drug Records, a Decision Log, and a public request form.
3. Configure the event listener described in [Ambiguous setup](docs/ambiguous-setup.md).
4. Treat each form response as a source-backed research request, not a clinical question.

See [examples](examples/) for portable templates. The materials here intentionally contain no patient data, controlled-access data, API keys, or private correspondence.
