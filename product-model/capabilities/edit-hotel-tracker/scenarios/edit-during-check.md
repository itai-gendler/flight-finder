---
{
  "kind": "validation",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Member chooses Save while a check runs",
      "kind": "actor",
      "actor": "member",
      "entities": [],
      "contexts": {
        "web": {
          "place": "web::travel::hotel-tracker"
        }
      }
    },
    {
      "text": "The Product refuses with \"Wait for the current check to finish before editing\"",
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
          "place": "web::travel::hotel-tracker"
        }
      }
    }
  ]
}
---

# Editing during a check is refused

## Trigger

A check is running.

## Outcome

Nothing changes.
