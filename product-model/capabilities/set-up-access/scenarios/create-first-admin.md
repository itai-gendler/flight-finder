---
{
  "kind": "primary",
  "routes": {
    "cli": "Terminal"
  },
  "steps": [
    {
      "text": "The Instance operator runs access setup and enters the owner's name and a shared password",
      "kind": "actor",
      "actor": "instance-operator",
      "entities": [],
      "contexts": {
        "cli": {
          "place": "cli"
        }
      }
    },
    {
      "text": "The Product creates the Admin profile and stores the shared password",
      "kind": "product",
      "actor": "instance-operator",
      "entities": [
        {
          "entity": "admin",
          "effect": "creates",
          "facts": []
        },
        {
          "entity": "profile",
          "effect": "creates",
          "facts": [
            "Username"
          ],
          "with": "admin"
        },
        {
          "entity": "app-access",
          "effect": "changes",
          "facts": [
            "Shared password",
            "Owner set up"
          ]
        }
      ],
      "contexts": {
        "cli": {
          "place": "cli"
        }
      }
    }
  ]
}
---

# Create the first Admin and shared password

## Trigger

The Instance operator runs flight-finder access setup on a fresh instance.

## Outcome

The Admin profile exists and the shared password opens the app.
