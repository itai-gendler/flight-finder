---
{
  "domain": "cars",
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "apps/web/src/lib/cars/store.ts#createCarCatalogSearch"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "apps/web/src/lib/cars/types.ts"
    }
  ]
}
---

# Rental search

A car rental search of DiscoverCars, Auto Europe or both, independent of flights and hotels. A rental tracker's checks are rental searches too.

## Information kept

- **Pickup** — the catalog airport or city location
- **Return** — the catalog return location
- **Pickup time** — local pickup date and time
- **Return time** — local return date and time
- **Driver age** — the driver's age
- **Residence country** — the driver's country of residence
- **Licence years** — years holding a licence
- **Providers** — DiscoverCars, Auto Europe or both
- **Requested extras** — seats, additional drivers and a chosen protection product
- **Currency** — the price currency
- **Offers** — verified offers with rental total, payment timing, deposit, excess, policies and requirements
- **Unverified candidates** — advertised prices without enough evidence, shown for inspection only
- **Provider errors** — each provider failure
- **Offers checked** — how many visible offers were checked and whether the limit was reached
- **Tracking closed** — whether new trackers can no longer start from this search
- **Imported link** — the rental link the search was imported from, if any
- **Owner** — the profile it belongs to

## States

### Queued

Waiting to run.

### Running

Providers are being checked.

### Completed

Finished, possibly with provider errors.

### Failed

Could not complete.

### Cancelled

Stopped explicitly, or because its tracker changed.
