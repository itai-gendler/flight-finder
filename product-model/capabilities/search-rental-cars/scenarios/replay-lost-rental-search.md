---
{
  "kind": "edge",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Member recovers the saved request after a reload",
      "kind": "actor",
      "actor": "member",
      "entities": [],
      "contexts": {
        "web": {
          "place": "web::travel::cars"
        }
      }
    },
    {
      "text": "The request identity matches a search already started, so the Product returns that search",
      "kind": "condition",
      "entities": [
        {
          "entity": "rental-search",
          "effect": "reads",
          "facts": []
        }
      ],
      "contexts": {
        "web": {
          "place": "web::travel::cars"
        }
      }
    }
  ]
}
---

# A lost acknowledgement is recovered

## Trigger

The browser lost the reply to a started search.

## Outcome

The original search is shown; no second search starts.

## Edge cases

- Recovery needs browser session storage; reusing an identity for different criteria is refused.
