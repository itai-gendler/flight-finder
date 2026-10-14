---
{
  "kind": "primary",
  "routes": {
    "cli": "Terminal"
  },
  "steps": [
    {
      "text": "The Instance operator runs access device with a profile id and an optional name",
      "kind": "actor",
      "actor": "instance-operator",
      "entities": [
        {
          "entity": "profile",
          "effect": "reads",
          "facts": [
            "Username"
          ]
        }
      ],
      "contexts": {
        "cli": {
          "place": "cli"
        }
      }
    },
    {
      "text": "The Product creates an API device token for it and prints it",
      "kind": "product",
      "actor": "instance-operator",
      "entities": [
        {
          "entity": "device-token",
          "effect": "creates",
          "facts": [
            "Name",
            "Profile",
            "Scope",
            "Token"
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

# Create a device token

## Trigger

The Instance operator wants a terminal client to reach a private instance.

## Outcome

The token is printed once; clients send it as FLIGHT_FINDER_TOKEN.
