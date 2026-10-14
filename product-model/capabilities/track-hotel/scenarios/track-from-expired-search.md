---
{
  "kind": "validation",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Member chooses Track on an offer from that search",
      "kind": "actor",
      "actor": "member",
      "entities": [],
      "contexts": {
        "web": {
          "place": "web::travel::hotels"
        }
      }
    },
    {
      "text": "The Product refuses with \"Search expired; search again\"",
      "kind": "condition",
      "entities": [
        {
          "entity": "hotel-search",
          "effect": "reads",
          "facts": []
        }
      ],
      "contexts": {
        "web": {
          "place": "web::travel::hotels"
        }
      }
    }
  ]
}
---

# An old search cannot start tracking

## Trigger

The search finished more than a day ago.

## Outcome

No tracker is created; the Member searches again.
