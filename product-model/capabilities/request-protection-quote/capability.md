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
      "target": "apps/web/src/app/api/cars/search/[id]/protection/route.ts"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "apps/web/src/lib/cars/store.ts#createCarProtectionRecheck"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "apps/web/src/components/cars/CarProtectionChoices.tsx"
    }
  ]
}
---

# Request a protection quote

Review an observed protection product for a verified base rental and request a fresh quote with it. It neither reserves a car nor buys coverage.
