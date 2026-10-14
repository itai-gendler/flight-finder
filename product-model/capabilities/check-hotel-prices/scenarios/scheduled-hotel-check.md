---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "A tracking hotel tracker is due",
      "kind": "condition",
      "unattended": true,
      "entities": [
        {
          "entity": "hotel-tracker",
          "effect": "reads",
          "facts": [
            "Check interval",
            "Last checked"
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
      "text": "The Product runs a hotel search for the tracked stay",
      "kind": "product",
      "entities": [
        {
          "entity": "hotel-search",
          "effect": "creates",
          "facts": [
            "Destination",
            "Stay dates",
            "Rooms and guests",
            "Currency",
            "Sources",
            "Filters",
            "Owner"
          ],
          "to": "Queued"
        }
      ],
      "contexts": {
        "web": {
          "place": "web::travel::hotel-tracker"
        }
      }
    },
    {
      "text": "The Product records the matching offers",
      "kind": "product",
      "entities": [
        {
          "entity": "hotel-search",
          "effect": "changes",
          "facts": [
            "Offers",
            "Provider errors",
            "Progress"
          ],
          "from": "Queued",
          "to": "Completed"
        },
        {
          "entity": "hotel-price-observation",
          "effect": "creates",
          "facts": [
            "Stay dates",
            "Total price",
            "Currency",
            "Seller",
            "Room",
            "Rate",
            "Refundable",
            "Breakfast",
            "Match",
            "Eligible",
            "Observed at",
            "Booking link"
          ]
        },
        {
          "entity": "hotel-tracker",
          "effect": "changes",
          "facts": [
            "Latest price",
            "Historical low",
            "Target armed",
            "Last checked"
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
      "text": "The price is at or below the armed target, so the Product raises a target alert",
      "kind": "product",
      "entities": [
        {
          "entity": "price-alert",
          "effect": "creates",
          "facts": [
            "Message",
            "Recipients"
          ],
          "to": "Pending"
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

# Scheduled check reaches the target

## Trigger

A tracking hotel tracker is due.

## Outcome

The new price is in the history and a target alert waits for delivery; the target re-arms only after a complete check above it.
