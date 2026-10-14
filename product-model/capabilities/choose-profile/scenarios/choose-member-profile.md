---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Member chooses their profile from the picker",
      "kind": "actor",
      "actor": "member",
      "entities": [
        {
          "entity": "profile",
          "effect": "reads",
          "facts": [
            "Display name",
            "Avatar"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::travel::profile-picker"
        }
      }
    },
    {
      "text": "The Product selects that profile for this browser",
      "kind": "product",
      "actor": "member",
      "entities": [
        {
          "entity": "browser-session",
          "effect": "changes",
          "facts": [
            "Selected profile"
          ]
        },
        {
          "entity": "profile",
          "effect": "reads",
          "facts": []
        }
      ],
      "contexts": {
        "web": {
          "place": "web::travel::profile-picker"
        }
      }
    }
  ]
}
---

# Choose a profile

## Trigger

An admitted browser reaches "Who's using Flight Finder?".

## Outcome

The browser uses the chosen profile; a member lands on their trackers and Admin on the Admin dashboard.

## Edge cases

- With no profiles yet the picker says "No profiles yet."
