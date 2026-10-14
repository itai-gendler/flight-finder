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
      "target": "apps/web/src/app/api/queries/route.ts#POST"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "apps/web/src/components/FlightPicker.tsx"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "apps/web/src/components/ConfirmationCard.tsx"
    }
  ]
}
---

# Track flights

Select up to the configured number of flights per route and start tracking. Each route and date becomes a flight tracker, grouped on one chart, optionally comparing prices from other countries.
