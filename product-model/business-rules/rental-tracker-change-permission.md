---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "rental-tracker",
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

# Only Admin or the owning member changes a rental tracker

Admin may change any rental tracker; a member changes their own. Scheduled checks update trackers on their own.
