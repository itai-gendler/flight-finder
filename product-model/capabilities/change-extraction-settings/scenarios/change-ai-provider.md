---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "Admin chooses a provider, model and interval in Extraction and saves",
      "kind": "actor",
      "actor": "admin",
      "entities": [
        {
          "entity": "instance-settings",
          "effect": "reads",
          "facts": [
            "AI provider",
            "Model",
            "Check interval"
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
      "text": "The Product saves the extraction settings and reschedules checks",
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
            "Check interval",
            "Default currency",
            "Default search method"
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

# Change the AI provider and model

## Trigger

Admin switches provider in Settings.

## Outcome

Later parsing and extraction use the new provider; the scheduled interval applies at once.

## Edge cases

- Local providers list the models their server reports; unreachable servers show an error.
