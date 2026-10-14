---
{
  "kind": "validation",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Member tries to track an unverified candidate",
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
      "text": "The Product refuses with \"This quote cannot be tracked\" and the reasons",
      "kind": "condition",
      "entities": [
        {
          "entity": "rental-search",
          "effect": "reads",
          "facts": [
            "Unverified candidates"
          ]
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

# An unverified offer cannot be tracked

## Trigger

The offer lacks evidence for its total.

## Outcome

No tracker is created; the candidate stays inspectable.

## Edge cases

- An imported rental can only be tracked in contract mode.
- A search whose tracking was closed cannot start new trackers.
