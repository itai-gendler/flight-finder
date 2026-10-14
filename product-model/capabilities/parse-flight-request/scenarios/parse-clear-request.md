---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Member types the trip and presses Enter",
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
      "text": "The Product asks the configured language model to read it into routes, dates, flexibility, cabin and filters",
      "kind": "product",
      "actor": "member",
      "entities": [],
      "contexts": {
        "web": {
          "place": "web::travel::flights"
        }
      }
    },
    {
      "text": "The reading is confident, so the Product shows the request for review",
      "kind": "condition",
      "actor": "member",
      "entities": [],
      "contexts": {
        "web": {
          "place": "web::travel::flights"
        }
      }
    }
  ]
}
---

# A clear request is understood

## Trigger

A Member types a trip on Flights.

## Outcome

The reviewed request shows routes, dates, flexibility and filters with Show available flights.
