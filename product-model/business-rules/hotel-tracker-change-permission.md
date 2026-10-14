---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "hotel-tracker",
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

# Only Admin or the owning member changes a hotel tracker

Admin may change any hotel tracker; a member changes their own. Scheduled checks update trackers on their own.
