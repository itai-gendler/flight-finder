---
{
  "kind": "primary",
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
            "Next attempt",
            "Recipients"
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
      "text": "The Product sends it to each enabled recipient channel and records each acceptance",
      "kind": "product",
      "entities": [
        {
          "entity": "notification-channel",
          "effect": "reads",
          "facts": [
            "Type",
            "Settings"
          ]
        },
        {
          "entity": "price-alert",
          "effect": "changes",
          "facts": [
            "Delivered channels"
          ],
          "from": "Pending",
          "to": "Delivered"
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

# Deliver a pending alert

## Trigger

A price alert is pending while scraping is on.

## Outcome

The alert reaches its channels and shows as delivered on the tracker.
