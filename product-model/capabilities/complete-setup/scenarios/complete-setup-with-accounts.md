---
{
  "kind": "alternative",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "Admin turns on accounts in the Accounts step and completes setup",
      "kind": "actor",
      "actor": "admin",
      "entities": [],
      "contexts": {
        "web": {
          "place": "web::administration::setup"
        }
      }
    },
    {
      "text": "The Product saves the configuration, turns on multi-user mode and gives existing flight trackers to Admin",
      "kind": "product",
      "actor": "admin",
      "entities": [
        {
          "entity": "instance-settings",
          "effect": "changes",
          "facts": [
            "AI provider",
            "Model",
            "Provider credentials",
            "Community sharing",
            "Public site URL",
            "Setup complete",
            "Multi-user mode"
          ]
        },
        {
          "entity": "flight-tracker",
          "effect": "changes",
          "facts": [
            "Owner"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::administration::setup"
        }
      }
    }
  ]
}
---

# Complete setup with household accounts

## Trigger

Admin wants separate profiles.

## Outcome

Setup is complete and household profiles are on.
