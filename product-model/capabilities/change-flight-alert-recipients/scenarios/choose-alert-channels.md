---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Member chooses Choose channels, ticks channels and saves",
      "kind": "actor",
      "actor": "member",
      "entities": [
        {
          "entity": "notification-channel",
          "effect": "reads",
          "facts": [
            "Label",
            "Type"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::travel::flight-tracker"
        }
      }
    },
    {
      "text": "The Product saves the tracker's recipients",
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

# Choose channels

## Trigger

A Member wants a tracker's alerts on particular channels.

## Outcome

Only the chosen channels receive this tracker's alerts.
