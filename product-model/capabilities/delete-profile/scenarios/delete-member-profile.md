---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "Admin chooses Delete beside a member profile and confirms",
      "kind": "actor",
      "actor": "admin",
      "entities": [
        {
          "entity": "profile",
          "effect": "reads",
          "facts": [
            "Username",
            "Display name"
          ]
        },
        {
          "entity": "member",
          "effect": "reads",
          "facts": []
        }
      ],
      "contexts": {
        "web": {
          "place": "web::administration::users"
        }
      }
    },
    {
      "text": "The Product deletes the profile and keeps its trackers without an owner",
      "kind": "product",
      "actor": "admin",
      "entities": [
        {
          "entity": "member",
          "effect": "removes"
        },
        {
          "entity": "profile",
          "effect": "removes",
          "with": "member"
        },
        {
          "entity": "hotel-tracker",
          "effect": "changes",
          "facts": [
            "Owner"
          ]
        },
        {
          "entity": "rental-tracker",
          "effect": "changes",
          "facts": [
            "Owner"
          ]
        },
        {
          "entity": "flight-tracker",
          "effect": "changes",
          "facts": [
            "Owner"
          ]
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

# Delete a profile

## Trigger

Someone has left the household.

## Outcome

The profile is gone from the picker; its trackers remain for Admin.

## Edge cases

- The Admin profile cannot be deleted.
