---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "flight-tracker",
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
      "target": "apps/web/src/lib/query-auth.ts#authorizeMutation"
    }
  ]
}
---

# Only Admin or the owning member deletes a flight tracker

Admin may delete any flight tracker; a member deletes the trackers their profile owns.
