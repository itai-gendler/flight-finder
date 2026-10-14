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
      "target": "apps/web/src/app/api/cars/search/route.ts"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "apps/web/src/lib/cars/store.ts#createCarCatalogSearch"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "apps/web/src/components/cars/CarSearchForm.tsx"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "apps/web/src/components/cars/CarResults.tsx"
    }
  ]
}
---

# Search rental cars

Search DiscoverCars, Auto Europe or both from catalog pickup and return locations, local dates and times and driver details. Results show verified offers, unverified candidates and provider failures.
