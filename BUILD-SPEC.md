# BUILD SPEC - Skeleton Crew (Kiroween D4) - desk intake pack

[MUSEai]@{role:{challenge-entries-manager-d4}}
status: FROZEN variant | build window: > 2026-11-08 -> 2026-12-04T14:00PT
route: Desk a440bcb2 => Jules-on-issues (producer MUST = Jules) => termux-monorepo PR/CI/merge => artifact sync here => D4 seat verifies

## Sources (evidence)
- proposal: termux-monorepo docs/proposals/active/kiroween-delphi-concept-skeleton-crew/RFP.md (generated 2026-10-30T23:44:05Z)
- pass: kiroween-delphi-concept {round1 TIE 23.269 | debate 23.288 skeleton-crew #1 | priors 19/17/14}
- repo: created 2026-10-30T23:55:28Z in-period (window 2026-10-30T09:00PT..2026-12-04T14:00PT), scaffold 6b99cd4c
- rules: /.kiro at root (NOT gitignored) + LICENSE + public repo + demo <3min public + functional URL + Kiro write-up

## Product
CMDB/reconciliation viewer, minimal spec-first crew {ingest -> reconcile -> report}, READ-ONLY everywhere (no write/mutation action exposed by any component).

## Shape (Skeleton Crew category: foundation + 2 distinct apps / 2 folders)
- foundation/ : inventory schema (JSON) + source-adapter interface + reconciliation rules engine + fixture inventory + stamped conflict report output (JSON + sha256 stamp)
- apps/conflict-viewer/ : app 1 - inventory list + conflict matrix + evidence-stamp detail (static web app reading foundation output)
- apps/stamped-report/ : app 2 - renders the stamped reconciliation report (static web app)

## Constraints
- zero external services / zero secrets; runs locally; apps deployable as static site (functional URL)
- Kiro artifacts maintained in /.kiro {specs, steering, hooks} as build evidence
- pre-existing input DISCLOSED only: CMDB design doc patterns (monorepo); all code new in-period
- fallback (RFP alt): single-source viewer if reconciliation slips; stamped report stays demo centerpiece

## Tasks (Jules issue-sized, sequential T1 -> {T2,T3} -> T4)
- T1 foundation: schema + fixture + reconcile engine (CLI: fixture in -> stamped report JSON out)
- T2 conflict-viewer: consumes T1 output; list/matrix/detail views
- T3 stamped-report: consumes T1 output; report view w/ stamp + sha
- T4 integration: end-to-end run + test suites + README Kiro-usage write-up completion

## Acceptance (test suites from frozen plan; receipts REQUIRED - unreceipted = 0 passes)
- S1 spec-pack completeness: inventory schema + reconciliation rules present and parse
- S2 reconciliation run vs seeded fixture emits a stamped conflict report
- S3 read-only guard: no write/mutation action exposed by any agent/component
- every suite result carries receipt {command, exit_code, output sha256, code_paths}

## Submission pack (D4 seat owns, post-build)
demo video <3min public | functional app URL | Devpost text + /.kiro + LICENSE check | Kiro write-up final | deadline 2026-12-04T14:00PT
