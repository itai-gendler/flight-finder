---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "price-rule",
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
          "verb": "has",
          "entity": "flight-tracker"
        },
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
      "target": "apps/web/src/lib/notifications/rules/store.ts#updatePriceRules"
    }
  ]
}
---

# Only Admin or the tracker's owner changes its price rules

Price rules are edited by Admin or the member who owns the flight tracker.
