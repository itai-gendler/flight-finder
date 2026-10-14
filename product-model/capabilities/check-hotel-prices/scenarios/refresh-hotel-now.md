---
{
  "kind": "alternative",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Member chooses Refresh",
      "kind": "actor",
      "actor": "member",
      "entities": [],
      "contexts": {
        "web": {
          "place": "web::travel::hotel-tracker"
        }
      }
    },
    {
      "text": "The Product queues a check for the tracker, reusing one already queued",
      "kind": "product",
      "actor": "member",
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
      "actor": "member",
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
            "Last checked"
          ]
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

# Refresh a hotel tracker

## Trigger

A Member wants a current price.

## Outcome

The check runs and the page updates when it finishes.

## Edge cases

- Refresh is unavailable while the tracker is paused.
