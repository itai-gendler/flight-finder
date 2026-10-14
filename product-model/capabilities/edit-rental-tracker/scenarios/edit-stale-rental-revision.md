---
{
  "kind": "validation",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Member saves settings loaded before another change",
      "kind": "actor",
      "actor": "member",
      "entities": [],
      "contexts": {
        "web": {
          "place": "web::travel::rental-tracker"
        }
      }
    },
    {
      "text": "The revision no longer matches, so the Product refuses with \"Rental settings changed; refresh before trying this action again\"",
      "kind": "condition",
      "actor": "member",
      "entities": [
        {
          "entity": "rental-tracker",
          "effect": "reads",
          "facts": [
            "Revision"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::travel::rental-tracker"
        }
      }
    }
  ]
}
---

# A stale revision is refused

## Trigger

The tracker changed since it was loaded.

## Outcome

Nothing changes; the current settings are shown for review.
