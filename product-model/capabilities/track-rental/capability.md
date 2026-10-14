---
{
  "availability": [
    {
      "place": "web::travel"
    }
  ],
  "domain": "cars",
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "apps/web/src/app/api/cars/route.ts#POST"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "apps/web/src/lib/cars/store.ts#createCarTracker"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "apps/web/src/components/cars/useCarCreation.ts"
    }
  ]
}
---

# Track a rental

Track a verified offer: best mode follows the cheapest qualifying offer across the selected providers, contract mode follows the selected rental contract. Set a target, new-low alerts and a check interval.
