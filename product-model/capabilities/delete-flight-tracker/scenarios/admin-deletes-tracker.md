---
{
  "kind": "alternative",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "Admin chooses Delete for a tracker group and confirms",
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
      "text": "The Product deletes the trackers with their price history",
      "kind": "product",
      "actor": "admin",
      "entities": [
        {
          "entity": "flight-tracker",
          "effect": "removes",
          "from": "Paused"
        },
        {
          "entity": "fare-observation",
          "effect": "removes",
          "with": "flight-tracker"
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

# Admin deletes a tracker

## Trigger

Admin reviews Tracked Queries.

## Outcome

The tracker group is deleted.
