# Ambiguous setup

## Minimum workspace structure

Create a research wiki space containing:

- Research Home
- Four-Role Coordination Plan
- Software Stack for Breast-Cancer Metabolism and Drug Analysis
- Breast Tumor and Matched-Normal Genomic Data Access
- WHO Essential Medicines: Chemical and Pharmacology Data Register
- Prominent Breast-Cancer Metabolism Papers: Metadata-Driven Top 100
- Evidence Inbox, Candidate Drug Records, Pathway and Phenotype Map, and Decision Log

Create one task for each role and one public long-text form titled **Request a Breast-Cancer Metabolism Evidence Brief**. The form should collect a required research question, optional non-identifying context, and an optional contact email.

## Event handling

On a new form response:

1. Create an auditable research task containing the response ID and non-sensitive request text.
2. Dispatch a role-specific handoff to each of the four roles.
3. Create a source-linked evidence brief page and link it from the task and Evidence Inbox.
4. Add the completed brief to a public **Published Evidence Briefs** index.
5. When the response contains a valid email address, send one completion email containing the specific brief URL and the research-only boundary. Never send email to any other address.

The form confirmation should say **Processing...** and link to the published-brief index. Ambiguous's standard public-form UI does not currently keep a browser-side spinner open until a dynamically created brief is complete; that exact behaviour requires a custom public frontend that submits to Ambiguous and polls a status endpoint.

## Local credential hygiene

Store Ambiguous credentials only in local ignored configuration or environment variables. Never add a credential, response export, or controlled dataset to the repository.
