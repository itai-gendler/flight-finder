---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "Admin chooses a profile as Owner and chooses Reassign",
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
          "place": "web::travel::hotel-tracker"
        }
      }
    },
    {
      "text": "The Product moves the tracker, withdraws pending alerts and cancels queued checks",
      "kind": "product",
      "actor": "admin",
      "entities": [
        {
          "entity": "hotel-tracker",
          "effect": "changes",
          "facts": [
            "Owner"
          ]
        },
        {
          "entity": "price-alert",
          "effect": "changes",
          "facts": [],
          "from": "Pending",
          "to": "Withdrawn"
        },
        {
          "entity": "hotel-search",
          "effect": "changes",
          "facts": [],
          "from": "Queued",
          "to": "Cancelled"
        }
      ],
      "contexts": {
        "web": {
          "place": "web::travel::hotel-tracker"
        }
      }
    }
  ]
}
---

# Reassign a hotel tracker

## Trigger

Admin opens another profile's hotel tracker.

## Outcome

The tracker belongs to the chosen profile; its pending alerts and queued checks are dropped.
