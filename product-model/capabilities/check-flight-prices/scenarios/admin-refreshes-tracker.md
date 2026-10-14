---
{
  "kind": "alternative",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "Admin chooses refresh for a tracker group",
      "kind": "actor",
      "actor": "admin",
      "entities": [],
      "contexts": {
        "web": {
          "place": "web::administration::tracked-queries"
        }
      }
    },
    {
      "text": "The Product checks the group and records the fares",
      "kind": "product",
      "actor": "admin",
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
          "place": "web::administration::tracked-queries"
        }
      }
    }
  ]
}
---

# Admin refreshes a tracker

## Trigger

Admin reviews Tracked Queries.

## Outcome

The group is checked immediately.
