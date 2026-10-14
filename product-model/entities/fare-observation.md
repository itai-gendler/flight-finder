---
{
  "domain": "flights",
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "apps/web/prisma/schema.prisma"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "apps/web/src/lib/flight-pricing.ts"
    }
  ]
}
---

# Fare observation

One fare seen for one flight, travel date and country at one check. The chart, best price, history table and calendar are built from these.

## Information kept

- **Travel date** — the date the fare is for
- **Price** — the observed fare
- **Currency** — its currency
- **Airline** — the operating airline
- **Flight number** — the flight, when known
- **Departure time** — scheduled departure
- **Arrival time** — scheduled arrival
- **Stops** — number of stops
- **Layovers** — each layover airport and duration
- **Duration** — total travel time
- **Seats left** — seats left, when shown
- **Availability** — available or sold out
- **Country** — the VPN country it was observed from, or local
- **Observed at** — when it was observed
- **Booking link** — where to book it
