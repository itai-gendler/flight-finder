---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "Admin enters the style URL, resource origins, privacy and attribution links and saves",
      "kind": "actor",
      "actor": "admin",
      "entities": [
        {
          "entity": "instance-settings",
          "effect": "reads",
          "facts": [
            "Hotel map provider"
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
      "text": "The Product validates and saves the provider",
      "kind": "product",
      "actor": "admin",
      "entities": [
        {
          "entity": "instance-settings",
          "effect": "changes",
          "facts": [
            "Hotel map provider"
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

# Save a custom provider

## Trigger

Admin hosts their own map style.

## Outcome

Hotel maps load from the custom provider.
