---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "Admin chooses Edit, changes settings and chooses Save changes",
      "kind": "actor",
      "actor": "admin",
      "entities": [
        {
          "entity": "notification-channel",
          "effect": "reads",
          "facts": [
            "Type",
            "Label",
            "Settings"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::administration::notifications"
        }
      }
    },
    {
      "text": "The Product saves the channel, keeping secrets left blank",
      "kind": "product",
      "actor": "admin",
      "entities": [
        {
          "entity": "notification-channel",
          "effect": "changes",
          "facts": [
            "Label",
            "Settings",
            "Secret credentials"
          ]
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

# Edit a channel

## Trigger

Admin changes where a channel sends.

## Outcome

Later alerts use the new settings.
