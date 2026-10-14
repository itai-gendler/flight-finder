---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "Admin enters a username, display name and avatar in Add user",
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
      "text": "The Product creates the member profile",
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

# Add a user

## Trigger

Admin wants a profile for someone in the household.

## Outcome

The profile appears in the picker; it needs no password.
