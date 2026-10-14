---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Member chooses Pause and confirms",
      "kind": "actor",
      "actor": "member",
      "entities": [
        {
          "entity": "rental-tracker",
          "effect": "reads",
          "facts": [
            "Revision"
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
      "text": "The Product pauses the tracker, cancels running checks and withdraws pending alerts",
      "kind": "product",
      "actor": "member",
      "entities": [
        {
          "entity": "rental-tracker",
          "effect": "changes",
          "facts": [
            "Revision"
          ],
          "from": "Tracking",
          "to": "Paused"
        },
        {
          "entity": "rental-search",
          "effect": "changes",
          "facts": [],
          "from": "Running",
          "to": "Cancelled"
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

# Pause a rental tracker

## Trigger

A Member wants no checks for now.

## Outcome

The tracker is paused; running checks are cancelled and pending alerts withdrawn.
