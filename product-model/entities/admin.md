---
{
  "kind": "person",
  "acts": "external",
  "relations": [
    {
      "entity": "profile",
      "verb": "has",
      "cardinality": "one-to-one"
    },
    {
      "entity": "flight-tracker",
      "verb": "owns",
      "cardinality": "one-to-many"
    },
    {
      "entity": "hotel-tracker",
      "verb": "owns",
      "cardinality": "one-to-many"
    },
    {
      "entity": "hotel-search",
      "verb": "owns",
      "cardinality": "one-to-many"
    },
    {
      "entity": "rental-tracker",
      "verb": "owns",
      "cardinality": "one-to-many"
    },
    {
      "entity": "rental-search",
      "verb": "owns",
      "cardinality": "one-to-many"
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "apps/web/src/lib/admin-guard.ts#requireAdminApi"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "apps/web/src/lib/user-auth.ts#getCurrentUser"
    }
  ]
}
---

# Admin

The person using the Admin profile. The first profile created on an instance is Admin; Admin manages the instance, its settings, notification channels and member profiles, and can see and manage every tracker.
