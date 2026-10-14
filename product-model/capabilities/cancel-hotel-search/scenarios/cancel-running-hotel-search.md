---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Member chooses Cancel while the search runs",
      "kind": "actor",
      "actor": "member",
      "entities": [],
      "contexts": {
        "web": {
          "place": "web::travel::hotels"
        }
      }
    },
    {
      "text": "The Product cancels the search",
      "kind": "product",
      "actor": "member",
      "entities": [
        {
          "entity": "hotel-search",
          "effect": "changes",
          "facts": [],
          "from": "Running",
          "to": "Cancelled"
        }
      ],
      "contexts": {
        "web": {
          "place": "web::travel::hotels"
        }
      }
    }
  ]
}
---

# Cancel a running search

## Trigger

A hotel search is taking too long.

## Outcome

The search shows cancelled.
