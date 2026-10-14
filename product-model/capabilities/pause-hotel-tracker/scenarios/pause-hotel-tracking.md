---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Member chooses Pause",
      "kind": "actor",
      "actor": "member",
      "entities": [],
      "contexts": {
        "web": {
          "place": "web::travel::hotel-tracker"
        }
      }
    },
    {
      "text": "The Product pauses the tracker, withdraws its pending alerts and cancels queued checks",
      "kind": "product",
      "actor": "member",
      "entities": [
        {
          "entity": "hotel-tracker",
          "effect": "changes",
          "facts": [],
          "from": "Tracking",
          "to": "Paused"
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

# Pause a hotel tracker

## Trigger

A Member wants no checks for now.

## Outcome

The tracker shows paused; pending alerts and queued checks are dropped.
