---
{
  "kind": "edge",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Member recovers the saved creation request",
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
      "text": "The creation identity matches an existing tracker, so the Product returns it",
      "kind": "condition",
      "actor": "member",
      "entities": [
        {
          "entity": "rental-tracker",
          "effect": "reads",
          "facts": [
            "Label"
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

# A lost acknowledgement returns the same tracker

## Trigger

The browser lost the reply to Track.

## Outcome

The original tracker is shown; none is duplicated.

## Edge cases

- If that tracker was deleted, retrying does not recreate it.
