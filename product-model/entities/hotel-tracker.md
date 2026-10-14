---
{
  "domain": "hotels",
  "relations": [
    {
      "entity": "hotel-price-observation",
      "verb": "has",
      "cardinality": "one-to-many"
    },
    {
      "entity": "hotel-search",
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
      "target": "apps/web/src/lib/hotels/store.ts"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "apps/web/src/lib/hotels/domain.ts#evaluateHotelAlerts"
    }
  ]
}
---

# Hotel tracker

A tracked hotel stay: the cheapest qualifying offer at one property, or one particular room and rate.

## Information kept

- **Hotel name** — the property
- **Stay** — destination, dates and date mode
- **Rooms and guests** — rooms, adults and children's ages
- **Currency** — the price currency
- **Filters** — the stay filters it keeps
- **Source** — Google Hotels or Booking.com
- **Selected offer** — seller, room, rate, refundability and breakfast of the chosen offer
- **Match mode** — best offer at the property, or the particular room and rate
- **Target price** — alert at or below this total
- **New-low alerts** — whether a new historical low alerts
- **Approximate alerts** — whether approximate room and rate matches may alert
- **Check interval** — hours between checks, 1 to 24
- **Latest price** — the latest qualifying total
- **Historical low** — the lowest qualifying total seen
- **Target armed** — whether the next price at or below target alerts
- **Last checked** — when it was last checked
- **Last error** — the last check error
- **Owner** — the profile it belongs to

## States

### Tracking

Checked on its interval.

### Paused

No checks or alerts until resumed.
