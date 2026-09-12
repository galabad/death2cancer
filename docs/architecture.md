# Architecture

```text
Public request form
        ↓
Ambiguous task + audit record
        ↓
  ┌─────┼────────┬──────────┐
  ↓     ↓        ↓          ↓
software data    medicine   literature
role     role    role       role
  └─────┴────────┴──────────┘
        ↓
Orchestrator: evidence triangulation
        ↓
Evidence Inbox → Candidate Drug Record → linked evidence brief
```

Each role owns a bounded knowledge area. The Orchestrator checks provenance and evidence boundaries before writing shared Ambiguous artifacts. Every brief should preserve the question, sources, dates, data/tool versions, model/population, finding, limitations, privacy tier, and next action.

The project is deliberately not a single unconstrained chatbot. Its value comes from using the research workspace itself as durable context: specialist pages, source records, task history, and a decision log.
