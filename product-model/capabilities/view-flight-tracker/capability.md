---
{
  "availability": [
    {
      "place": "web::travel"
    }
  ],
  "domain": "flights",
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "apps/web/src/app/q/[id]/page.tsx"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "apps/web/src/components/PriceChart.tsx"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "apps/web/src/components/BestPrice.tsx"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "apps/web/src/components/PriceCalendar.tsx"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "apps/web/src/lib/flight-pricing.ts"
    }
  ]
}
---

# View a flight price chart

Open a tracker's chart: price evolution per airline, best current price, price history with booking links, a fare calendar and markers for filter changes.
