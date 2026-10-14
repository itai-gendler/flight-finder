---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Member chooses Pause tracking on a tracker in the list",
      "kind": "actor",
      "actor": "member",
      "entities": [],
      "contexts": {
        "web": {
          "place": "web::travel::flights"
        }
      }
    },
    {
      "text": "The Product pauses the tracker and its group",
      "kind": "product",
      "actor": "member",
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
          "place": "web::travel::flights"
        }
      }
    }
  ]
}
---

# Pause tracking

## Trigger

A Member wants to stop checks for now.

## Outcome

The group shows Paused and is not checked.
