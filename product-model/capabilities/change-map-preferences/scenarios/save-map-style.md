---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Member chooses a map style in map preferences and saves",
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
      "text": "The Product saves the preference on the profile",
      "kind": "product",
      "actor": "member",
      "entities": [
        {
          "entity": "profile",
          "effect": "changes",
          "facts": [
            "Map style",
            "Map shown"
          ]
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

# Save a map style

## Trigger

A Member prefers another map style.

## Outcome

Hotel results use the saved style.

## Edge cases

- On a single-user instance the preference is kept in the current browser only.
- A preference changed elsewhere meanwhile is refused with a request to reload.
