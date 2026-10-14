---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "Admin chooses Disable",
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
      "text": "The Product disables the channel",
      "kind": "product",
      "actor": "admin",
      "entities": [
        {
          "entity": "notification-channel",
          "effect": "changes",
          "facts": [],
          "from": "Enabled",
          "to": "Disabled"
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

# Disable a channel

## Trigger

Admin pauses a channel.

## Outcome

The channel shows disabled and receives nothing.
