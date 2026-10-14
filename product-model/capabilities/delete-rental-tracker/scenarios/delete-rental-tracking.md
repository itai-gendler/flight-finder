---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Member chooses Delete and confirms",
      "kind": "actor",
      "actor": "member",
      "entities": [
        {
          "entity": "rental-tracker",
          "effect": "reads",
          "facts": [
            "Revision"
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
      "text": "The Product deletes the tracker with its price history",
      "kind": "product",
      "actor": "member",
      "entities": [
        {
          "entity": "rental-tracker",
          "effect": "removes",
          "from": "Tracking"
        },
        {
          "entity": "rental-price-observation",
          "effect": "removes",
          "with": "rental-tracker"
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

# Delete a rental tracker

## Trigger

A Member no longer needs a tracker.

## Outcome

The tracker and its history are gone.
