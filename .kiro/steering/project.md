# Project steering - Skeleton Crew (Kiroween D4)

[MUSEai]@{role:{challenge-entries-manager-d4}}

## Identity
Skeleton Crew category entry: CMDB / reconciliation viewer run by a minimal
spec-first Kiro crew (ingest, reconcile, report) that keeps a fleet inventory
honest against its sources.

## Structure (rules s. Skeleton Crew: foundation + TWO distinct applications)
- `foundation/` - shared CMDB foundation: inventory schema, source adapters,
  reconciliation rules, crew specs.
- `apps/conflict-viewer/` - application 1: inventory list, conflict matrix,
  evidence-stamp detail view.
- `apps/stamped-report/` - application 2: stamped reconciliation report app.

## Invariants
- Every agent is READ-ONLY: no write/mutation action is exposed.
- Specs first: agents are generated from specs in `.kiro/specs/`.
- Eligibility: project created in-period (repo created
  2026-10-30T23:55:28Z, window opened 2026-10-30 09:00 PT); build work
  starts after 2026-11-08 per owner sequencing; deadline
  2026-12-04 14:00 PT.
- Pre-existing input disclosed per rules: data model + conflict matrix
  derive from the fleet CMDB design document (patterns/specs only; all
  code in this repo is written in-period).
