---
{
  "domain": "flights",
  "relations": [
    {
      "entity": "fare-observation",
      "verb": "has",
      "cardinality": "one-to-many"
    },
    {
      "entity": "tracker-edit",
      "verb": "has",
      "cardinality": "one-to-many"
    },
    {
      "entity": "price-rule",
      "verb": "has",
      "cardinality": "one-to-many"
    },
    {
      "entity": "price-alert",
      "verb": "has",
      "cardinality": "one-to-many"
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "apps/web/prisma/schema.prisma"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "apps/web/src/app/api/queries/route.ts"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "apps/web/src/app/api/queries/[id]/route.ts"
    }
  ]
}
---

# Flight tracker

One tracked route and travel date (or date window) whose prices Flight Finder checks on a schedule. A search over several routes or dates creates one tracker per route and date, grouped on one chart.

## Information kept

- **Request** — the original natural-language request or the details entered
- **Route** — origin and destination airports
- **Travel dates** — outbound and return dates
- **Flexibility** — days either side of the travel dates
- **Trip type** — round trip or one way
- **Cabin class** — the cabin prices are checked for
- **Currency** — the currency prices are compared in
- **Max price** — the price filter applied to shown fares
- **Max stops** — the stops filter
- **Max duration** — the trip duration filter, 1 to 48 hours
- **Preferred airlines** — the airlines filter
- **Departure window** — any, morning, afternoon, evening or red-eye
- **Strict departure window** — whether only flights inside the departure window are kept
- **Label** — an optional name of up to 60 characters
- **Check interval** — 1, 3, 6, 12 or 24 hours, or following the instance default
- **Price sources** — the ordered sources this tracker uses
- **Comparison countries** — countries whose prices are compared through the VPN
- **Notification recipients** — household defaults, or chosen notification channels
- **Tracking ends** — the date after which the tracker stops
- **Last check** — when prices were last checked and whether the check succeeded, partly succeeded or failed
- **Tracker group** — the sibling trackers created by the same search
- **Imported link** — the booking link the tracker was imported from, if any
- **Owner** — the profile it belongs to on a multi-user instance

## States

### Tracking

Prices are checked on schedule.

### Paused

Checks and alerts are stopped until resumed.

### Expired

The departure day has passed; checks have stopped.
