---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Member chooses Show available flights",
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
      "text": "The Product starts a flight search for the request",
      "kind": "product",
      "actor": "member",
      "entities": [
        {
          "entity": "flight-fare-search",
          "effect": "creates",
          "facts": [
            "Request"
          ],
          "to": "Pending"
        }
      ],
      "contexts": {
        "web": {
          "place": "web::travel::flights"
        }
      }
    },
    {
      "text": "The Product looks up fares for every route and date pair",
      "kind": "product",
      "actor": "member",
      "entities": [
        {
          "entity": "flight-fare-search",
          "effect": "changes",
          "facts": [],
          "from": "Pending",
          "to": "Running"
        }
      ],
      "contexts": {
        "web": {
          "place": "web::travel::flights"
        }
      }
    },
    {
      "text": "The Product lists the available flights",
      "kind": "product",
      "actor": "member",
      "entities": [
        {
          "entity": "flight-fare-search",
          "effect": "changes",
          "facts": [
            "Available flights"
          ],
          "from": "Running",
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
      "text": "The Member reviews the available flights",
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
    }
  ]
}
---

# Show available flights

## Trigger

A reviewed flight request is on screen.

## Outcome

Available flights per route and date are listed with prices, times and stops.

## Edge cases

- Leaving and reopening the page resumes the same search.
- A round trip whose fare cannot be retrieved shows a separate one-way estimate that cannot be tracked.
