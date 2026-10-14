---
{
  "kind": "validation",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Visitor enters the shared password",
      "kind": "actor",
      "actor": "visitor",
      "entities": [],
      "contexts": {
        "web": {
          "place": "web::app-access::open-flight-finder"
        }
      }
    },
    {
      "text": "The address is not one the instance accepts for login, so the Product refuses with \"This address is not configured for login\"",
      "kind": "condition",
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
          "place": "web::app-access::open-flight-finder"
        }
      }
    }
  ]
}
---

# Entering from an unconfigured address is refused

## Trigger

A Visitor opens the instance through a tunnel or hostname that is not configured for login.

## Outcome

Nothing is admitted; the screen names the terminal command that configures the address.
