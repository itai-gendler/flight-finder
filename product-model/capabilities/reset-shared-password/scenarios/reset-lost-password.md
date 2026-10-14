---
{
  "kind": "primary",
  "routes": {
    "cli": "Terminal"
  },
  "steps": [
    {
      "text": "The Instance operator runs access reset and types a new password, which is not echoed",
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
      "text": "The Product replaces the shared password and revokes every session and passkey",
      "kind": "product",
      "actor": "instance-operator",
      "entities": [
        {
          "entity": "app-access",
          "effect": "changes",
          "facts": [
            "Shared password"
          ]
        },
        {
          "entity": "browser-session",
          "effect": "removes"
        },
        {
          "entity": "passkey",
          "effect": "removes"
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

# Reset a lost shared password

## Trigger

Nobody remembers the shared password.

## Outcome

Only the new password opens the app; everyone enters again and saves passkeys again.
