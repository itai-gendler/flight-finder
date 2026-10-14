---
{
  "domain": "flights",
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "apps/web/src/lib/notifications/rules/store.ts#updatePriceRules"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "apps/web/src/lib/notifications/rules/evaluate.ts#evaluatePriceRule"
    }
  ]
}
---

# Price rule

A custom alert rule on a flight tracker: a target price or a drop, for the tracker's lowest fare or one previously selected flight.

## Information kept

- **Scope** — the lowest fare in the tracker, or one previously selected flight
- **Currency** — the rule's three-letter currency
- **Target price** — alert at or below this price
- **Absolute drop** — alert on a drop of at least this amount
- **Percentage drop** — alert on a drop of at least this percentage, below 100
- **Cooldown** — minutes between alerts, 0 to 10080
- **Enabled** — whether the rule is active
- **Baseline** — the price drops are measured from: the price when saved, then the last triggered drop
