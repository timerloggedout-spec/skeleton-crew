# Requirements - CMDB foundation (scaffold stub, build > 2026-11-08)

1. Inventory schema: assets, sources, evidence stamps.
2. Source adapters ingest inventories read-only.
3. Reconciliation rules compare inventory vs sources and emit conflicts.
4. Test suites (from the frozen variant plan):
   - spec-pack completeness: schema + rules present and parse
   - reconciliation run vs seeded fixture emits a stamped conflict report
   - read-only guard: no write/mutation action exposed by any agent
