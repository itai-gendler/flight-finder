---
{
  "kind": "validation",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "Admin adds a user with an existing username",
      "kind": "actor",
      "actor": "admin",
      "entities": [
        {
          "entity": "profile",
          "effect": "reads",
          "facts": [
            "Username"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::administration::users"
        }
      }
    },
    {
      "text": "The Product refuses with \"Username already taken\"",
      "kind": "condition",
      "entities": [],
      "contexts": {
        "web": {
          "place": "web::administration::users"
        }
      }
    }
  ]
}
---

# A taken username is refused

## Trigger

The username already exists.

## Outcome

Nothing is created.

## Edge cases

- Usernames are 2 to 32 letters, numbers, underscores, dots or dashes.
