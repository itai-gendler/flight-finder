---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Member opens the hotel tracker",
      "kind": "actor",
      "actor": "member",
      "entities": [
        {
          "entity": "hotel-tracker",
          "effect": "reads",
          "facts": [
            "Hotel name",
            "Stay",
            "Rooms and guests",
            "Latest price",
            "Match mode"
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
      "text": "The Member reads the price history",
      "kind": "actor",
      "actor": "member",
      "entities": [
        {
          "entity": "hotel-price-observation",
          "effect": "reads",
          "facts": [
            "Stay dates",
            "Total price",
            "Seller",
            "Room",
            "Match",
            "Eligible"
          ]
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

# View price history

## Trigger

A Member opens a hotel tracker.

## Outcome

Every recorded offer is shown with seller, room, policies and whether it was an approximate match.

## Edge cases

- Without a notification channel the page suggests configuring one in Settings.
