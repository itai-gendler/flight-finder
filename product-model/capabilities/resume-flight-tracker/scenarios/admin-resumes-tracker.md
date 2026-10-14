---
{
  "kind": "alternative",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "Admin chooses Resume for a paused group",
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
      "text": "The Product resumes the group",
      "kind": "product",
      "actor": "admin",
      "entities": [
        {
          "entity": "flight-tracker",
          "effect": "changes",
          "facts": [],
          "from": "Paused",
          "to": "Tracking"
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

# Admin resumes a tracker

## Trigger

Admin reviews Tracked Queries.

## Outcome

The group is tracked again.
