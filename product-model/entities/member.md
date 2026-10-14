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
      "target": "apps/web/src/lib/user-auth.ts#getCurrentProfile"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "apps/web/src/lib/hotels/access.ts#hotelActor"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "apps/web/src/lib/cars/access.ts#carActor"
    }
  ]
}
---

# Member

A household member using an ordinary profile on a multi-user instance. Members keep their own trackers and preferences.
