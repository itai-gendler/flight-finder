---
{
  "kind": "alternative",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Member chooses Enter flight details manually, picks airports and dates and chooses Show available flights",
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
      "text": "The Product starts a flight search for those details",
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
      "text": "The Product runs the lookups and lists the available flights",
      "kind": "product",
      "actor": "member",
      "entities": [
        {
          "entity": "flight-fare-search",
          "effect": "changes",
          "facts": [
            "Available flights"
          ],
          "from": "Pending",
          "to": "Completed"
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

# Search from details entered manually

## Trigger

A Member prefers to enter flight details without AI.

## Outcome

Available flights are listed as for a described trip.

## Edge cases

- Origin and destination must differ; dates cannot be in the past and the return must follow departure.
