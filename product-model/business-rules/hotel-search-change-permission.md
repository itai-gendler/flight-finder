---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "hotel-search",
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
      "target": "apps/web/src/lib/hotels/access.ts#assertHotelOwner"
    }
  ]
}
---

# Only Admin or the owning member runs or cancels a hotel search

A hotel search is worked on for the member who started it or for Admin; tracker checks run on their own.
