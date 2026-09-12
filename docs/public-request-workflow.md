# Public request workflow

## Public URLs

- Request form: <https://app.ambiguous.ai/f/death2cancer/request-breast-cancer-metabolism-evidence-brief>
- Published briefs: <https://app.ambiguous.ai/wiki/breast-cancer-metabolism-research-public/published-evidence-briefs>

## User experience

1. A visitor submits a research question, optional non-identifying context, and optional email address.
2. The form confirms receipt with **Processing...** and a link to the published-brief index.
3. The listener creates an auditable Ambiguous task, coordinates the four roles, and writes a source-linked brief.
4. The listener adds the brief to the public index.
5. If the visitor supplied an email address, it receives one completion message containing that brief's direct URL.

## Safety controls

- The form warns against patient-identifying information, medical records, controlled-access data, credentials, and urgent medical questions.
- Briefs are research-only evidence maps, never treatment, dosing, or patient-specific recommendations.
- Completion email is sent only to the address in the originating response. It contains a result URL and research boundary, not confidential data.

## Optional custom frontend

For a persistent busy indicator and automatic redirect to a request-specific result page, implement a separate public client that:

1. submits to the Ambiguous form endpoint;
2. receives a request/status identifier;
3. polls a read-only status endpoint; and
4. redirects only when the evidence-brief URL is published.

Do not expose Ambiguous agent credentials to that client. A server-side relay or tightly scoped public endpoint is required.
