---
{
  "domain": "cars",
  "relations": [
    {
      "entity": "rental-price-observation",
      "verb": "has",
      "cardinality": "one-to-many"
    },
    {
      "entity": "rental-search",
      "verb": "checks",
      "cardinality": "one-to-many"
    },
    {
      "entity": "price-alert",
      "verb": "raises",
      "cardinality": "one-to-many"
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "apps/web/src/lib/cars/store.ts#createCarTracker"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "apps/web/src/lib/cars/store.ts#editCarTracker"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "apps/web/src/lib/cars/alerts.ts#evaluateCarAlerts"
    }
  ]
}
---

# Rental tracker

A tracked car rental: the cheapest qualifying offer across the selected providers (best mode) or one rental contract (contract mode).

## Information kept

- **Label** — its name, by default pickup → return
- **Rental criteria** — locations, times, driver details, providers and extras
- **Tracking mode** — best or contract
- **Selected contract** — the provider and contract followed in contract mode
- **Currency** — the price currency
- **Target price** — alert at or below this total
- **New-low alerts** — whether a new low alerts
- **Check interval** — hours between checks
- **Revision** — the settings revision every change must name
- **Latest price** — the latest verified total
- **Historical low** — the lowest verified total seen
- **Target armed** — whether the next price at or below target alerts
- **Last checked** — when it was last checked
- **Last error** — the last check error
- **Owner** — the profile it belongs to

## States

### Tracking

Checked on its interval.

### Paused

No checks or pending alerts until resumed.
