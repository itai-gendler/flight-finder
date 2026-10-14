---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "rental-tracker",
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
      "target": "apps/web/src/lib/cars/access.ts#assertCarOwner"
    }
  ]
}
---

# Only Admin or the owning member sees a rental tracker

A rental tracker and its history are visible to Admin and to the member whose profile owns it; to anyone else it does not exist.
