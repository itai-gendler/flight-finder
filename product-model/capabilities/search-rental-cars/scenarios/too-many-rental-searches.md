---
{
  "kind": "validation",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Member starts another search",
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
      "text": "The Product refuses with \"Three car searches are already active; wait or cancel one\"",
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

# A fourth active rental search is refused

## Trigger

Three of the profile's rental searches are still running.

## Outcome

Nothing new is queued.
