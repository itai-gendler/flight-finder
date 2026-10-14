---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "Admin chooses a type, fills its settings and chooses Add channel",
      "kind": "actor",
      "actor": "admin",
      "entities": [],
      "contexts": {
        "web": {
          "place": "web::administration::notifications"
        }
      }
    },
    {
      "text": "The Product saves the channel with its secrets encrypted",
      "kind": "product",
      "actor": "admin",
      "entities": [
        {
          "entity": "notification-channel",
          "effect": "creates",
          "facts": [
            "Type",
            "Label",
            "Settings",
            "Secret credentials"
          ],
          "to": "Enabled"
        }
      ],
      "contexts": {
        "web": {
          "place": "web::administration::notifications"
        }
      }
    }
  ]
}
---

# Add a channel

## Trigger

Admin wants alerts on a phone.

## Outcome

The channel is enabled and receives alerts.

## Edge cases

- Pushover emergency priority needs retry seconds of at least 30 and expiry of at most 10800.
