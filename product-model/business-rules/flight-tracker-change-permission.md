---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "flight-tracker",
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
      "target": "apps/web/src/lib/query-auth.ts#authorizeMutation"
    }
  ]
}
---

# Only Admin or the owning member changes a flight tracker

Admin may change any flight tracker; a member changes the trackers their profile owns. Scheduled checks change trackers on their own.
