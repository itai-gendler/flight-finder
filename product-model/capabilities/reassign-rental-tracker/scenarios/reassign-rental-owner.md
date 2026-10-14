---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "Admin chooses a profile and chooses Reassign tracker",
      "kind": "actor",
      "actor": "admin",
      "entities": [
        {
          "entity": "profile",
          "effect": "reads",
          "facts": [
            "Display name"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::travel::rental-tracker"
        }
      }
    },
    {
      "text": "The Product moves the tracker as a new revision and withdraws pending alerts",
      "kind": "product",
      "actor": "admin",
      "entities": [
        {
          "entity": "rental-tracker",
          "effect": "changes",
          "facts": [
            "Owner",
            "Revision"
          ]
        },
        {
          "entity": "price-alert",
          "effect": "changes",
          "facts": [],
          "from": "Pending",
          "to": "Withdrawn"
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

# Reassign a rental tracker

## Trigger

Admin opens another profile's rental tracker.

## Outcome

The tracker belongs to the chosen profile.
