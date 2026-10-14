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

# Pause a rental tracker

Stop future checks and pending alerts. Messages already sent cannot be recalled.
