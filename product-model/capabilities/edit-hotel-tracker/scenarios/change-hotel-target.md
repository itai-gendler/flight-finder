---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Member changes the target price and chooses Save",
      "kind": "actor",
      "actor": "member",
      "entities": [
        {
          "entity": "hotel-tracker",
          "effect": "reads",
          "facts": [
            "Target price",
            "Check interval"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::travel::hotel-tracker"
        }
      }
    },
    {
      "text": "The Product saves the alerts, re-arms the target and withdraws pending alerts",
      "kind": "product",
      "actor": "member",
      "entities": [
        {
          "entity": "hotel-tracker",
          "effect": "changes",
          "facts": [
            "Target price",
            "New-low alerts",
            "Approximate alerts",
            "Check interval",
            "Target armed"
          ]
        },
        {
          "entity": "price-alert",
          "effect": "changes",
          "facts": [],
          "from": "Pending",
          "to": "Withdrawn"
        }
      ],
      "contexts": {
        "web": {
          "place": "web::travel::hotel-tracker"
        }
      }
    }
  ]
}
---

# Change the target price

## Trigger

A Member sets a new target.

## Outcome

The target is armed again and pending alerts are withdrawn.

## Edge cases

- Changing whether approximate matches may alert also restarts the historical low.
