---
{
  "kind": "primary",
  "result": "achieved",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Member types the trip and presses Enter",
      "kind": "actor",
      "actor": "member",
      "capability": "parse-flight-request",
      "entities": [],
      "contexts": {
        "web": {
          "place": "web::travel::flights"
        }
      }
    },
    {
      "text": "The Product shows the reviewed request with Show available flights",
      "kind": "product",
      "actor": "member",
      "capability": "parse-flight-request",
      "entities": [],
      "contexts": {
        "web": {
          "place": "web::travel::flights"
        }
      }
    },
    {
      "text": "The Member chooses Show available flights",
      "kind": "actor",
      "actor": "member",
      "capability": "search-flight-fares",
      "entities": [],
      "contexts": {
        "web": {
          "place": "web::travel::flights"
        }
      }
    },
    {
      "text": "The Product looks up fares and lists the available flights",
      "kind": "product",
      "actor": "member",
      "capability": "search-flight-fares",
      "entities": [
        {
          "entity": "flight-fare-search",
          "effect": "creates",
          "facts": [
            "Request",
            "Available flights"
          ],
          "to": "Completed"
        }
      ],
      "contexts": {
        "web": {
          "place": "web::travel::flights"
        }
      }
    },
    {
      "text": "The Member selects flights and chooses Track flights",
      "kind": "actor",
      "actor": "member",
      "capability": "track-flights",
      "entities": [],
      "contexts": {
        "web": {
          "place": "web::travel::flights"
        }
      }
    },
    {
      "text": "The Product creates the flight trackers",
      "kind": "product",
      "actor": "member",
      "capability": "track-flights",
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

# Describe, search and track

## Trigger

A Member types a trip on Flights.

## Outcome

The chosen flights are tracked.
