---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "Admin pastes the resulting URL in Reach it from other devices and chooses Save URL",
      "kind": "actor",
      "actor": "admin",
      "entities": [
        {
          "entity": "instance-settings",
          "effect": "reads",
          "facts": [
            "Public site URL"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::administration::instance-settings"
        }
      }
    },
    {
      "text": "The Product saves the public URL",
      "kind": "product",
      "actor": "admin",
      "entities": [
        {
          "entity": "instance-settings",
          "effect": "changes",
          "facts": [
            "Public site URL"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::administration::instance-settings"
        }
      }
    }
  ]
}
---

# Save the public URL

## Trigger

Admin has made the instance reachable.

## Outcome

Phones, QR codes and alert links use the saved address.

## Edge cases

- Leaving it empty uses the address each device connects on.
