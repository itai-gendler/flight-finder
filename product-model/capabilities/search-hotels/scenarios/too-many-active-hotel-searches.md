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
          "place": "web::travel::hotels"
        }
      }
    },
    {
      "text": "The Product refuses with \"Three hotel searches are already active; wait or cancel one\"",
      "kind": "condition",
      "entities": [
        {
          "entity": "hotel-search",
          "effect": "reads",
          "facts": []
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

# A fourth active search is refused

## Trigger

Three of the profile's hotel searches are still running.

## Outcome

Nothing new is queued.
