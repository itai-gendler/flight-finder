---
{
  "kind": "primary",
  "routes": {
    "cli": "Terminal"
  },
  "steps": [
    {
      "text": "The Instance operator runs access origin with the full address, including a nonstandard port",
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
      "text": "The Product saves it as the instance's login address",
      "kind": "product",
      "actor": "instance-operator",
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
        "cli": {
          "place": "cli"
        }
      }
    }
  ]
}
---

# Configure the login address

## Trigger

The instance is reached through a tunnel or custom hostname.

## Outcome

Signing in works from that address; temporary tunnel addresses need configuring again when they change.

## Edge cases

- Changing the hostname changes where passkeys work; passkeys are saved again at the new address.
