---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "hotel-tracker",
      "effect": "reads"
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

# Only Admin or the owning member sees a hotel tracker

A hotel tracker and its history are visible to Admin and to the member whose profile owns it; to anyone else it does not exist.
