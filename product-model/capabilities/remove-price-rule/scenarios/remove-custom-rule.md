---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Member chooses Remove rule and saves",
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
      "text": "The Product removes the rule",
      "kind": "product",
      "actor": "member",
      "entities": [
        {
          "entity": "price-rule",
          "effect": "removes"
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

# Remove a rule

## Trigger

A Member no longer wants a rule.

## Outcome

The rule is gone.
