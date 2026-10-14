---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Member chooses Add rule, sets a target price and saves",
      "kind": "actor",
      "actor": "member",
      "entities": [],
      "contexts": {
        "web": {
          "place": "web::travel::flight-tracker"
        }
      }
    },
    {
      "text": "The Product saves the rule with the current price as its baseline",
      "kind": "product",
      "actor": "member",
      "entities": [
        {
          "entity": "price-rule",
          "effect": "creates",
          "facts": [
            "Scope",
            "Currency",
            "Target price",
            "Absolute drop",
            "Percentage drop",
            "Cooldown",
            "Enabled",
            "Baseline"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::travel::flight-tracker"
        }
      }
    }
  ]
}
---

# Add a target price rule

## Trigger

A Member wants an alert below a price.

## Outcome

The rule is saved and alerts when the lowest fare reaches the target.
