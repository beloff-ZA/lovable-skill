# Prompt patterns and external lookup

## GitHub-first inspection
Confirm repository and synced branch/commit. Use GitHub web editor (period key on a repository), local IDE, or an authorised GitHub connector. Inspect route registration, target component, immediate imports and relevant data hook. Browser DevTools can provide selected element, console stack, failing network request and status. Never include secret keys, auth tokens or customer data in prompts. Line numbers are hints; use symbols and commit identifiers to anchor changes. If direct code editing is authorised and suitable, use a reviewed diff and normal version-control workflow instead of paying Lovable to rediscover it. Verify sync before subsequent Build prompts.

## Scoped change template
Objective: [one coherent outcome]
Evidence: [route, repo revision, exact path/symbol, error or screenshot]
Change: [expected behaviour, existing utilities to reuse]
Boundaries: [allowed files/areas, protected behaviour]
Acceptance: [observable criteria and required checks]
Stop: [report blocker rather than broaden materially; no unrelated changes]

Example (illustrative paths): /credit-optimisation In src/components/calls/CallCard.tsx, change StatusBadge's pending variant to the existing amber token. Preserve all status logic and layouts. Check pending and completed states. No unrelated changes.

## Bug example
/credit-optimisation On /visits/new, submission returns a missing technician_id error. Inspect handleSubmit in the verified VisitForm component and its existing auth/data contract. If the missing field is confirmed, use the correct authorised technician identifier; do not assume the auth user ID equals the technician ID. Preserve validation and RLS. Test a valid and invalid submission. Report if the schema or permissions require a wider change.

## Extensive build example
Plan an internal service desk: shell and routes; users/roles/tickets schema and RLS; ticket create/list/detail; assignment/status transitions; notifications; reporting; release verification. Group create/list if they reuse stable schema and components. Separate uncertain payment/email integrations, shared permissions migrations and unrelated redesign. Provide one executable prompt per coherent slice with prerequisites and acceptance criteria. Use existing project conventions rather than imposing invented paths.
