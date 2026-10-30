# Skeleton Crew - Kiroween 2026 (D4)

A CMDB / reconciliation viewer run by a minimal crew: a tiny set of
spec-first Kiro agents (ingest, reconcile, report) that keep a fleet
inventory honest against its sources.

**Category:** Skeleton Crew - foundation plus TWO distinct applications:

- `foundation/` - CMDB foundation: inventory schema, source adapters,
  reconciliation rules, crew specs.
- `apps/conflict-viewer/` - application 1: inventory list, conflict
  matrix, evidence-stamp detail view.
- `apps/stamped-report/` - application 2: stamped reconciliation report.

## Status

- Variant FROZEN 2026-10-30 (skeleton-crew, Delphi pass
  `kiroween-delphi-concept`).
- Repo created 2026-10-30T23:55:28Z - inside the submission period
  (opened 2026-10-30 09:00 PT, closes 2026-12-04 14:00 PT).
- Scaffold only. Build starts after 2026-11-08; submission deadline
  2026-12-04 14:00 PT.

## Built with Kiro

Kiro usage write-up: STUB - completed during the build window.
Specs, steering, and hooks live in `/.kiro` (committed, not gitignored),
per the Kiroween deliverable rules.

## Disclosure (pre-existing work, per official rules)

Data model and conflict matrix derive from the fleet's CMDB design
document (design patterns only). All code in this repository is new,
written inside the submission period. Standard frameworks/libraries
may be used.

## License

MIT - see `LICENSE`.
