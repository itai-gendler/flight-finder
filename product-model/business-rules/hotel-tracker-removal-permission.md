---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "hotel-tracker",
      "effect": "removes"
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

# Only Admin or the owning member deletes a hotel tracker

Admin may delete any hotel tracker; a member deletes their own.
