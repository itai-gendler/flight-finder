---
{
  "domain": "cars",
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "apps/web/prisma/schema.prisma"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "apps/web/src/lib/cars/pricing.ts#assessCarPrice"
    }
  ]
}
---

# Rental price observation

One rental offer seen for a rental tracker at one check, with its price evidence.

## Information kept

- **Provider** — DiscoverCars or Auto Europe
- **Rental total** — the total for the requested rental
- **Currency** — its currency
- **Payment timing** — what is paid now and at pickup
- **Deposit** — the deposit, shown apart from the total
- **Excess** — the excess, shown apart from the total
- **Fuel and mileage** — fuel and mileage policies
- **Driver requirements** — age and licence requirements
- **Extras** — each selected extra and its supported price
- **Eligible** — whether the offer is verified and may alert
- **Reasons** — why it is not eligible
- **Observed at** — when it was seen
- **Contract** — the rental contract it belongs to
