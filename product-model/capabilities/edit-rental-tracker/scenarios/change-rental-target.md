---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Member changes the target and saves the settings",
      "kind": "actor",
      "actor": "member",
      "entities": [
        {
          "entity": "rental-tracker",
          "effect": "reads",
          "facts": [
            "Revision",
            "Target price"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::travel::rental-tracker"
        }
      }
    },
    {
      "text": "The Product saves the settings as a new revision",
      "kind": "product",
      "actor": "member",
      "entities": [
        {
          "entity": "rental-tracker",
          "effect": "changes",
          "facts": [
            "Label",
            "Target price",
            "New-low alerts",
            "Check interval",
            "Revision",
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
          "place": "web::travel::rental-tracker"
        }
      }
    }
  ]
}
---

# Change the rental target

## Trigger

A Member sets a new target.

## Outcome

The target is re-armed, running checks are cancelled and pending alerts withdrawn.
