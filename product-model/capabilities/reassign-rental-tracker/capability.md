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
      "target": "apps/web/src/components/cars/CarManagement.tsx"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "apps/web/src/lib/cars/store.ts#editCarTracker"
    }
  ]
}
---

# Reassign a rental tracker

Admin moves a rental tracker to another profile on a multi-user instance.
