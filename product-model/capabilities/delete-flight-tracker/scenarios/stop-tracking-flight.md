---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Member chooses Stop tracking and confirms Yes, delete",
      "kind": "actor",
      "actor": "member",
      "entities": [],
      "contexts": {
        "web": {
          "place": "web::travel::flight-tracker"
        }
      }
    },
    {
      "text": "The Product deletes the tracker with its price history",
      "kind": "product",
      "actor": "member",
      "entities": [
        {
          "entity": "flight-tracker",
          "effect": "removes",
          "from": "Tracking"
        },
        {
          "entity": "fare-observation",
          "effect": "removes",
          "with": "flight-tracker"
        }
      ],
      "contexts": {
        "web": {
          "place": "web::travel::flight-tracker"
        }
      }
    }
  ]
}
---

# Stop tracking

## Trigger

A Member no longer needs a tracker.

## Outcome

The tracker and its price history are gone; this cannot be undone.

## Edge cases

- Removing a group from the list deletes every tracker in the group.
