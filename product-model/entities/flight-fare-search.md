---
{
  "domain": "flights",
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "apps/web/src/app/api/preview/route.ts"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "apps/web/src/lib/travel/preview.ts"
    }
  ]
}
---

# Flight search

A look-up of current fares for a reviewed flight request before anything is tracked. It runs in the background so the page can be left and reopened.

## Information kept

- **Request** — the reviewed routes, dates, filters, cabin and currency
- **Available flights** — flights found per route and date, with price, airline, times, stops and booking link
- **Error** — why the search failed

## States

### Pending

Accepted and waiting to run.

### Running

Fares are being looked up.

### Completed

Available flights are ready to pick from.

### Failed

The search could not complete.
