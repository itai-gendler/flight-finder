---
{
  "kind": "alternative",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Member chooses Refresh now on the chart",
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
      "text": "The Product checks the tracker group immediately and records the fares",
      "kind": "product",
      "actor": "member",
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
    }
  ]
}
---

# Refresh now

## Trigger

A Member wants current prices.

## Outcome

The chart shows the new check.

## Edge cases

- A second refresh within a minute is refused with "Try again in a minute."
