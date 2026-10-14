---
{
  "kind": "alternative",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Member chooses Choose channels with none ticked and saves",
      "kind": "actor",
      "actor": "member",
      "entities": [],
      "contexts": {
        "web": {
          "place": "web::travel::flight-tracker"
        }
      }
    },
    {
      "text": "The Product saves an empty recipient list, which mutes the tracker",
      "kind": "product",
      "actor": "member",
      "entities": [
        {
          "entity": "flight-tracker",
          "effect": "changes",
          "facts": [
            "Notification recipients"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::travel::flight-tracker"
        }
      }
    }
  ]
}
---

# Mute a tracker

## Trigger

A Member wants no alerts from one tracker.

## Outcome

The tracker raises no alerts.

## Edge cases

- A selected channel that no longer exists must be removed before saving.
