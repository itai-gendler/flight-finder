---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "Admin chooses a provider and model, enters any key, chooses community sharing and the public address, and completes setup",
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
      "text": "The Product saves the configuration and marks setup complete",
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
            "Setup complete"
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

# Complete setup

## Trigger

Admin opens the app before setup is complete.

## Outcome

Setup is complete and Flights opens.

## Edge cases

- Ready subscription CLIs are listed first; testing a model selection saves nothing.
- Completing setup a second time is refused; settings change in the admin panel.
