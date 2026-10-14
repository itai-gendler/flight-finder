---
{
  "kind": "edge",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "A price alert is pending and due",
      "kind": "condition",
      "unattended": true,
      "entities": [
        {
          "entity": "price-alert",
          "effect": "reads",
          "facts": [
            "Next attempt"
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
      "text": "No channel accepts it, so the Product records the reason and schedules a retry",
      "kind": "product",
      "entities": [
        {
          "entity": "price-alert",
          "effect": "changes",
          "facts": [
            "Last error",
            "Next attempt"
          ]
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

# Delivery is retried

## Trigger

No enabled channel accepts the alert.

## Outcome

The alert stays pending with the reason and is retried five minutes later.

## Edge cases

- While scraping is paused, pending alerts wait.
