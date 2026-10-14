---
{
  "kind": "alternative",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "Admin chooses Pause for a tracker group",
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
      "text": "The Product pauses the group",
      "kind": "product",
      "actor": "admin",
      "entities": [
        {
          "entity": "flight-tracker",
          "effect": "changes",
          "facts": [],
          "from": "Tracking",
          "to": "Paused"
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

# Admin pauses a tracker

## Trigger

Admin reviews Tracked Queries.

## Outcome

The group is paused.
