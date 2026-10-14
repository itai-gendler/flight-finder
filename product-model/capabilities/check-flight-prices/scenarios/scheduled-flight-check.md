---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "A tracking flight tracker is due",
      "kind": "condition",
      "unattended": true,
      "entities": [
        {
          "entity": "flight-tracker",
          "effect": "reads",
          "facts": [
            "Check interval",
            "Last check"
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
      "text": "The Product checks the tracker's sources in order, from the local baseline and each comparison country, and records the fares",
      "kind": "product",
      "entities": [
        {
          "entity": "fare-observation",
          "effect": "creates",
          "facts": [
            "Travel date",
            "Price",
            "Currency",
            "Airline",
            "Flight number",
            "Departure time",
            "Arrival time",
            "Stops",
            "Layovers",
            "Duration",
            "Seats left",
            "Availability",
            "Country",
            "Observed at",
            "Booking link"
          ]
        },
        {
          "entity": "flight-tracker",
          "effect": "changes",
          "facts": [
            "Last check"
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
      "text": "The lowest fare beats the last alerted low by the alert thresholds, so the Product raises a new-low alert to the tracker's recipients",
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
        },
        {
          "entity": "instance-settings",
          "effect": "reads",
          "facts": [
            "Alert minimum drop",
            "Alert minimum percentage drop"
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

# Scheduled check finds a new low

## Trigger

A tracker is due for its interval while scraping is on.

## Outcome

New fares are in the history and a price alert waits for delivery.

## Edge cases

- When a source returns no flights the next source runs; flights filtered out by the tracker stop the chain.
- A partial check keeps the successful fares and reports the failed date, airline and failure category.
