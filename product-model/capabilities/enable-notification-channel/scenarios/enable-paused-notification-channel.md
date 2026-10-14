---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "Admin chooses Enable",
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
      "text": "The Product enables the channel",
      "kind": "product",
      "actor": "admin",
      "entities": [
        {
          "entity": "notification-channel",
          "effect": "changes",
          "facts": [],
          "from": "Disabled",
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

# Enable a channel

## Trigger

Admin turns a channel back on.

## Outcome

The channel receives alerts again.
