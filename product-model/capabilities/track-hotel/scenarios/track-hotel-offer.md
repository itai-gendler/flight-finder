---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Member chooses the match mode, a target price and alerts, then Track on an offer",
      "kind": "actor",
      "actor": "member",
      "entities": [
        {
          "entity": "hotel-search",
          "effect": "reads",
          "facts": [
            "Offers"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::travel::hotels"
        }
      }
    },
    {
      "text": "The Product creates a hotel tracker for that property and source, without the search budget",
      "kind": "product",
      "actor": "member",
      "entities": [
        {
          "entity": "hotel-tracker",
          "effect": "creates",
          "facts": [
            "Hotel name",
            "Stay",
            "Rooms and guests",
            "Currency",
            "Filters",
            "Source",
            "Selected offer",
            "Match mode",
            "Target price",
            "New-low alerts",
            "Approximate alerts",
            "Check interval",
            "Target armed",
            "Owner"
          ],
          "to": "Tracking"
        }
      ],
      "contexts": {
        "web": {
          "place": "web::travel::hotels"
        }
      }
    },
    {
      "text": "The Product opens the new tracker",
      "kind": "product",
      "actor": "member",
      "entities": [
        {
          "entity": "hotel-tracker",
          "effect": "reads",
          "facts": [
            "Hotel name"
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

# Track a hotel offer

## Trigger

A completed search lists offers.

## Outcome

The hotel tracker exists and its page opens.
