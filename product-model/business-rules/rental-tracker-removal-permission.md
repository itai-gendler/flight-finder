---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "rental-tracker",
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
      "target": "apps/web/src/lib/cars/access.ts#assertCarOwner"
    }
  ]
}
---

# Only Admin or the owning member deletes a rental tracker

Admin may delete any rental tracker; a member deletes their own.
