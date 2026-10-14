---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "rental-search",
      "effect": "changes"
    }
  ],
  "permits": [
    {
      "actors": [
        "admin"
      ]
    },
    {
      "related": [
        {
          "verb": "owns",
          "entity": "member"
        }
      ]
    },
    {
      "unattended": true
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "apps/web/src/lib/cars/access.ts#assertCarOwner"
    }
  ]
}
---

# Only Admin or the owning member runs or cancels a rental search

A rental search is worked on for the member who started it or for Admin; tracker checks run on their own.
