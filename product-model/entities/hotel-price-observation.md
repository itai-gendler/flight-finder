---
{
  "domain": "hotels",
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "apps/web/prisma/schema.prisma"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "apps/web/src/components/hotels/HotelDetail.tsx"
    }
  ]
}
---

# Hotel price observation

One offer seen for a hotel tracker at one check, kept in its price history.

## Information kept

- **Stay dates** — check-in and check-out
- **Total price** — the total including taxes and fees
- **Currency** — its currency
- **Seller** — who sells it
- **Room** — the room name, when known
- **Rate** — the rate name, when known
- **Refundable** — yes, no or unknown
- **Breakfast** — yes, no or unknown
- **Match** — exact or approximate
- **Eligible** — whether it qualifies for alerts
- **Observed at** — when it was seen
- **Booking link** — where to book it
