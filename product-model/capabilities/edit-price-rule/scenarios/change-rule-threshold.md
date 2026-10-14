---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Member changes a rule's drop and saves",
      "kind": "actor",
      "actor": "member",
      "entities": [
        {
          "entity": "price-rule",
          "effect": "reads",
          "facts": [
            "Scope",
            "Target price",
            "Absolute drop",
            "Percentage drop"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::travel::flight-tracker"
        }
      }
    },
    {
      "text": "The Product saves the rule",
      "kind": "product",
      "actor": "member",
      "entities": [
        {
          "entity": "price-rule",
          "effect": "changes",
          "facts": [
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

# Change a rule

## Trigger

A Member adjusts a rule.

## Outcome

Later checks use the new thresholds.

## Edge cases

- After the tracker's currency changes, a rule must be moved to the tracker currency or removed.
