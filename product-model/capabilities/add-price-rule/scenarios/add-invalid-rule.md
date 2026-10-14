---
{
  "kind": "validation",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Member adds a rule without any positive target or drop and saves",
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
      "text": "The Product refuses: at least one positive target or drop is required, percentage below 100 and cooldown 0 to 10080 minutes",
      "kind": "condition",
      "entities": [],
      "contexts": {
        "web": {
          "place": "web::travel::flight-tracker"
        }
      }
    }
  ]
}
---

# A rule without a threshold is refused

## Trigger

A Member saves a rule with no target or drop.

## Outcome

Nothing is saved.
