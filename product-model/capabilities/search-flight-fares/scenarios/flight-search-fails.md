---
{
  "kind": "edge",
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
      "text": "The Product starts the flight search",
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
      "text": "The Product cannot retrieve fares and shows \"Failed to search flights\"",
      "kind": "product",
      "actor": "member",
      "entities": [
        {
          "entity": "flight-fare-search",
          "effect": "changes",
          "facts": [
            "Error"
          ],
          "from": "Pending",
          "to": "Failed"
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

# The flight search fails

## Trigger

Fares cannot be retrieved.

## Outcome

The failure is shown; the request can be edited and searched again.

## Edge cases

- A search that takes too long reports "Flight search took too long."
