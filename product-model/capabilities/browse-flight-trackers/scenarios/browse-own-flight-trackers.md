---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Member opens Flights",
      "kind": "actor",
      "actor": "member",
      "entities": [],
      "contexts": {
        "web": {
          "place": "web::travel::flights"
        }
      }
    },
    {
      "text": "The Product lists the Member's own trackers, grouped by search",
      "kind": "product",
      "actor": "member",
      "entities": [
        {
          "entity": "flight-tracker",
          "effect": "reads",
          "facts": [
            "Route",
            "Travel dates",
            "Label",
            "Last check"
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

# Browse your flight trackers

## Trigger

A Member opens Flights.

## Outcome

The profile's trackers are listed as Tracking, Paused or Expired.

## Edge cases

- With none, the list says "No flight trackers yet."
