---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "Admin pastes the activation code and chooses Save code",
      "kind": "actor",
      "actor": "admin",
      "entities": [
        {
          "entity": "instance-settings",
          "effect": "reads",
          "facts": [
            "VPN provider"
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
      "text": "The Product saves the provider and code and checks the VPN is ready",
      "kind": "product",
      "actor": "admin",
      "entities": [
        {
          "entity": "instance-settings",
          "effect": "changes",
          "facts": [
            "VPN provider",
            "VPN activation code"
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

# Save the activation code

## Trigger

Admin wants country comparisons.

## Outcome

The code is saved encrypted and the VPN status is shown.

## Edge cases

- If readiness cannot be confirmed the code stays saved and the status says so.
