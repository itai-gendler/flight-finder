---
{
  "kind": "alternative",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "Admin changes limits, rate caps and allowed sources and chooses Save",
      "kind": "actor",
      "actor": "admin",
      "entities": [
        {
          "entity": "instance-settings",
          "effect": "reads",
          "facts": [
            "Extraction limits",
            "Allowed price sources"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::administration::extraction-config"
        }
      }
    },
    {
      "text": "The Product saves the configuration",
      "kind": "product",
      "actor": "admin",
      "entities": [
        {
          "entity": "instance-settings",
          "effect": "changes",
          "facts": [
            "Extraction limits",
            "Rate limits",
            "Allowed price sources",
            "Default country",
            "Theme"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::administration::extraction-config"
        }
      }
    }
  ]
}
---

# Change limits and allowed sources

## Trigger

Admin tunes extraction in Extraction Config.

## Outcome

Later searches and checks use the new limits and sources.
