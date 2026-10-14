---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Member selects flights, optionally picks countries to compare and chooses Track flights",
      "kind": "actor",
      "actor": "member",
      "entities": [
        {
          "entity": "flight-fare-search",
          "effect": "reads",
          "facts": [
            "Available flights"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::travel::flights"
        }
      }
    },
    {
      "text": "The Product creates a flight tracker per route and date, grouped together, recording the selected fares",
      "kind": "product",
      "actor": "member",
      "entities": [
        {
          "entity": "flight-tracker",
          "effect": "creates",
          "facts": [
            "Request",
            "Route",
            "Travel dates",
            "Flexibility",
            "Trip type",
            "Cabin class",
            "Currency",
            "Max price",
            "Max stops",
            "Max duration",
            "Preferred airlines",
            "Departure window",
            "Strict departure window",
            "Label",
            "Check interval",
            "Price sources",
            "Comparison countries",
            "Notification recipients",
            "Tracking ends",
            "Tracker group",
            "Owner"
          ],
          "to": "Tracking"
        },
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
          ],
          "with": "flight-tracker"
        }
      ],
      "contexts": {
        "web": {
          "place": "web::travel::flights"
        }
      }
    },
    {
      "text": "The created trackers are listed with links to their charts",
      "kind": "condition",
      "entities": [
        {
          "entity": "flight-tracker",
          "effect": "reads",
          "facts": [
            "Route",
            "Travel dates"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::travel::flights"
        }
      }
    }
  ]
}
---

# Track the selected flights

## Trigger

Available flights are listed.

## Outcome

Trackers exist for each selected route and date, with the selected fares as their first price history.

## Edge cases

- An imported link tracks exactly that itinerary; its first prices come from an immediate check, not the selection.
