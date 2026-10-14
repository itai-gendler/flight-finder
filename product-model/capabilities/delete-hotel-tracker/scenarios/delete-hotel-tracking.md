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
      "entities": [],
      "contexts": {
        "web": {
          "place": "web::travel::hotel-tracker"
        }
      }
    },
    {
      "text": "The Product deletes the tracker and its price history and returns to Hotels",
      "kind": "product",
      "actor": "member",
      "entities": [
        {
          "entity": "hotel-tracker",
          "effect": "removes",
          "from": "Tracking"
        },
        {
          "entity": "hotel-price-observation",
          "effect": "removes",
          "with": "hotel-tracker"
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

# Delete a hotel tracker

## Trigger

A Member no longer needs a tracker.

## Outcome

The tracker is gone and Hotels opens.
