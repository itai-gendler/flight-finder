---
{
  "kind": "alternative",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "Admin chooses an interval or Follow global for a tracker group",
      "kind": "actor",
      "actor": "admin",
      "entities": [],
      "contexts": {
        "web": {
          "place": "web::administration::tracked-queries"
        }
      }
    },
    {
      "text": "The Product saves the interval for the group",
      "kind": "product",
      "actor": "admin",
      "entities": [
        {
          "entity": "flight-tracker",
          "effect": "changes",
          "facts": [
            "Check interval"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::administration::tracked-queries"
        }
      }
    }
  ]
}
---

# Admin sets a tracker's interval

## Trigger

Admin reviews Tracked Queries.

## Outcome

The tracker group follows the chosen interval or the global one.
