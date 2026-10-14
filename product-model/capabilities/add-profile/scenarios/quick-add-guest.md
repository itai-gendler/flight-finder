---
{
  "kind": "alternative",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "Admin chooses the quick add guest button",
      "kind": "actor",
      "actor": "admin",
      "entities": [],
      "contexts": {
        "web": {
          "place": "web::administration::users"
        }
      }
    },
    {
      "text": "The Product creates the next free guest profile with an assigned avatar",
      "kind": "product",
      "actor": "admin",
      "entities": [
        {
          "entity": "member",
          "effect": "creates",
          "facts": []
        },
        {
          "entity": "profile",
          "effect": "creates",
          "facts": [
            "Username",
            "Display name",
            "Avatar"
          ],
          "with": "member"
        }
      ],
      "contexts": {
        "web": {
          "place": "web::administration::users"
        }
      }
    }
  ]
}
---

# Quick add a guest

## Trigger

Admin needs a profile quickly.

## Outcome

A guest profile with the next free guest name and an avatar exists.
