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
      "target": "apps/web/src/lib/cars/store.ts#editCarTracker"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "apps/web/src/components/cars/CarManagement.tsx"
    }
  ]
}
---

# Edit a rental tracker

Change a rental tracker's label, target price, new-low alerts and check interval. Rental criteria cannot change; create a new tracker instead.
