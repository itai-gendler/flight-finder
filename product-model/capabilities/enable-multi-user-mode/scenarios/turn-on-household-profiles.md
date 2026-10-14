---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "Admin chooses Enable multi user mode in Settings",
      "kind": "actor",
      "actor": "admin",
      "entities": [
        {
          "entity": "instance-settings",
          "effect": "reads",
          "facts": [
            "Multi-user mode"
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
      "text": "The Product turns on multi-user mode, gives existing trackers to Admin and withdraws pending alerts",
      "kind": "product",
      "actor": "admin",
      "entities": [
        {
          "entity": "instance-settings",
          "effect": "changes",
          "facts": [
            "Multi-user mode"
          ]
        },
        {
          "entity": "flight-tracker",
          "effect": "changes",
          "facts": [
            "Owner"
          ]
        },
        {
          "entity": "hotel-tracker",
          "effect": "changes",
          "facts": [
            "Owner"
          ]
        },
        {
          "entity": "rental-tracker",
          "effect": "changes",
          "facts": [
            "Owner"
          ]
        },
        {
          "entity": "price-alert",
          "effect": "changes",
          "facts": [],
          "from": "Pending",
          "to": "Withdrawn"
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

# Enable multi user mode

## Trigger

Admin wants separate profiles.

## Outcome

Profiles can be added; existing trackers belong to Admin.

## Edge cases

- Checks running at that moment are cancelled and can be refreshed.
- Enabling twice is refused.
