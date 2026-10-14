---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Member cancels the running search",
      "kind": "actor",
      "actor": "member",
      "entities": [],
      "contexts": {
        "web": {
          "place": "web::travel::rental-search"
        }
      }
    },
    {
      "text": "The Product cancels it",
      "kind": "product",
      "actor": "member",
      "entities": [
        {
          "entity": "rental-search",
          "effect": "changes",
          "facts": [],
          "from": "Running",
          "to": "Cancelled"
        }
      ],
      "contexts": {
        "web": {
          "place": "web::travel::rental-search"
        }
      }
    }
  ]
}
---

# Cancel a rental search

## Trigger

A rental search is still running.

## Outcome

The search is cancelled.
