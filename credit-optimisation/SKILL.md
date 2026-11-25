---
name: credit-optimisation
description: Use when planning or implementing Lovable features, scoped edits, debugging, refactoring or credit reviews where Build expenditure matters. Minimise discovery, rework and verification overhead while preserving correctness. Not for unrelated content generation.
---
# Credit optimisation v1.0

## Objective
Minimise total credits per accepted requirement, including planning, investigation, implementation, verification and rework. Preserve security, functionality, accessibility and data integrity. Do not claim guaranteed credit savings or enforceable prompt-level billing caps. Apply only to the requested task; do not modify code merely to optimise future costs without approval.

## 1. Select the cheapest suitable execution path
- Planning only: return a compact plan; do not edit. Prefer external GitHub/IDE investigation when evidence can be gathered there. Plan mode is not free; research subagents may add costs.
- Exact copy or trivial style change: suggest inline preview editing or a direct code edit if the user can safely do it; do not launch a second workflow unnecessarily.
- Clear, bounded implementation: proceed directly in Build mode; do not require a separate planning turn for every small change.
- Ambiguous bug, multi-domain feature or risky migration: investigate narrowly in Plan mode or externally first. Return a staged plan before implementation if the request does not already authorise it.
- Avoid /goal for routine work, broad autonomous audits, unnecessary image/video generation and speculative subagents. Use them only when justified or requested.

## 2. Locate before modifying
Use the supplied repository, branch/commit, route, file path, symbol and error evidence. Treat paths and diagnoses as hypotheses until verified against current code. Do not invent paths. If a project map exists, use its relevant entry rather than rebuilding it. Start with the exact file and relevant symbol or range where tools permit; read imports, callers, types or policies only when needed. Reuse observations within the current run; reread only changed or uncertain context. If the target is unknown, inspect the route registry or nearest directory, then run one targeted symbol/text search; widen progressively only when evidence warrants it. Exclude generated files, lockfiles, build outputs and dependencies unless implicated. Never perform a repository-wide scan by default. If evidence is missing and material, request the smallest useful missing detail or report the bounded investigation result.

## 3. Control scope and batch intelligently
Define expected result, allowed files/areas, protected behaviour, dependencies and acceptance checks. Make minimal coherent diffs; preserve existing utilities, styling, schemas, APIs and conventions. Group related edits that share context and tests. Split independent changes or risky integration boundaries; do not create needless micro-prompts or duplicate setup. If additional files are necessary, inspect only direct dependencies; explain material scope expansion and obtain approval when it exceeds the user's authorised change. No unsolicited redesign, dependency upgrade, cleanup, renaming, migrations or publishing. Never bypass tests, permissions, RLS or validation to save credits.

## 4. Large projects
Create an ordered dependency-aware plan: app shell/routing/theme; schema/auth/permissions; independently testable vertical workflows; external integrations; targeted polish and release checks. Combine UI and backend when the contract is stable and doing so avoids duplicate work; use mock UI then real wiring when UX or schema is uncertain. Label mocks and remove them before feature acceptance. For each slice specify target paths or clearly marked proposed paths, prerequisites, protected areas, acceptance criteria and checkpoint. Keep new components cohesive and reasonably small (roughly 150–250 lines is a review heuristic, not a hard limit); split by responsibility when justified, not by line count alone. Do not refactor stable large files solely for this rule. Maintain a small route/component/service index only if repeated navigation warrants it; update affected entries, not the whole map.

## 5. Evidence-led debugging and stopping rules
Start with exact reproduction, expected/actual result, console/network error, environment, last known good change and implicated symbol. Trace only the relevant path. State the evidence-backed hypothesis; change the smallest causal code. Run targeted checks, then the necessary integration or security tests proportional to risk. Do not repeatedly rerun unchanged tests or regenerate whole modules. After one failed correction, inspect the actual failure before retrying. After two unsuccessful hypotheses, or if a new subsystem is implicated, stop speculative edits, preserve a coherent state, report findings and propose the next targeted investigation. Do not suppress errors or replace live logic with mocks as a workaround. Do not claim a test passed unless executed or observed.

## 6. Verification and completion
Use existing lint/typecheck/test commands and targeted preview checks; expand when shared code, auth, data, payments or production behaviour is affected. Inspect changed diff for unintended changes. For risky work use a known good commit/version or draft where available; rollback only task-owned changes, never unrelated user work. Stop when acceptance criteria are satisfied, not when every imaginable improvement is exhausted. Report changed paths, checks actually run, unresolved issues and any necessary follow-up in a few lines. State actual credits only if available from billing; otherwise mark unknown. Do not run extra research solely to produce a cost estimate.

## 7. Credit guardrails
Use Low / Medium / High scope-risk labels only when helpful, based on known files, uncertainty, integration risk and test breadth; these are not credit forecasts. For high-risk work recommend a checkpoint and ask the user to review actual spend in the response menu. Keep long-run credit check-ins enabled; these are notification thresholds, not hard caps. Actual workspace/project/member limits are configured by authorised admins, not by this skill. Never change spend settings, monitoring, hosting, security controls or production availability without explicit approval. Prioritise Build savings; review Run costs separately when requested.

## 8. Optional references
Read only the relevant bundled file when needed: `prompt-patterns.md` for examples and external inspection; `measurement.md` for benchmarking and billing guidance. Do not load both by default. For routine edits apply this core playbook silently, without restating it.
