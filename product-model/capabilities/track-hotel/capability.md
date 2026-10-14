---
{
  "availability": [
    {
      "place": "web::travel"
    }
  ],
  "domain": "hotels",
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "apps/web/src/app/api/hotels/route.ts#POST"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "apps/web/src/lib/hotels/store.ts#createHotelTracker"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "apps/web/src/components/hotels/HotelOptions.tsx"
    }
  ]
}
---

# Track a hotel

Track an offer from a completed search: the best offer at that property, or the particular room and rate, with an optional target price and alerts.
