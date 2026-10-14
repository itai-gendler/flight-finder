---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Member opens the tracker's chart",
      "kind": "actor",
      "actor": "member",
      "entities": [
        {
          "entity": "flight-tracker",
          "effect": "reads",
          "facts": [
            "Route",
            "Travel dates",
            "Label",
            "Last check",
            "Tracking ends"
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
      "text": "The Product builds the chart and best price from the latest fare per flight, date and country, after the tracker's filters",
      "kind": "product",
      "actor": "member",
      "entities": [
        {
          "entity": "fare-observation",
          "effect": "reads",
          "facts": [
            "Price",
            "Airline",
            "Travel date",
            "Observed at",
            "Booking link"
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
      "text": "The Member reads the edit markers on the chart",
      "kind": "actor",
      "actor": "member",
      "entities": [
        {
          "entity": "tracker-edit",
          "effect": "reads",
          "facts": [
            "Edited at",
            "Summary"
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

# View the price chart

## Trigger

A Member opens a tracker.

## Outcome

Latest fares, history and edit markers are shown; each fare links to booking.

## Edge cases

- A failed or unsampled check can leave an older observation visible with its observation time.
- An expired tracker shows Expired instead of the days left.
