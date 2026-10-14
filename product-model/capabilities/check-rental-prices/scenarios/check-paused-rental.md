---
{
  "kind": "validation",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Member asks for a check",
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
      "text": "The Product refuses with \"Resume this car tracker before refreshing\"",
      "kind": "condition",
      "actor": "member",
      "entities": [
        {
          "entity": "rental-tracker",
          "effect": "reads",
          "facts": []
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

# A paused tracker cannot be checked

## Trigger

The tracker is paused.

## Outcome

No check runs.

## Edge cases

- A stale revision is refused with "Rental settings changed; refresh before trying this action again".
