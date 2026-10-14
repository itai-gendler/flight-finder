---
{
  "domain": "flights",
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "apps/web/src/app/api/queries/[id]/route.ts#PATCH"
    }
  ]
}
---

# Tracker edit

An entry in a flight tracker's edit history: a filter change shown as a marker on its price chart.

## Information kept

- **Edited at** — when the change was saved
- **Summary** — what changed, such as "Nonstop only enabled"
- **Changes** — each filter with its value before and after
- **Editor** — the profile that made the change
