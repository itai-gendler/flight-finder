---
{
  "kind": "alternative",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Member turns the map off in Account settings and saves",
      "kind": "actor",
      "actor": "member",
      "entities": [],
      "contexts": {
        "web": {
          "place": "web::travel::account-settings"
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
          "place": "web::travel::account-settings"
        }
      }
    }
  ]
}
---

# Change map preferences in Account settings

## Trigger

A Member edits Account & appearance.

## Outcome

Hotel results use the saved preference.
