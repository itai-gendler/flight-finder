---
{
  "kind": "primary",
  "result": "achieved",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Member searches a stay",
      "kind": "actor",
      "actor": "member",
      "capability": "search-hotels",
      "entities": [],
      "contexts": {
        "web": {
          "place": "web::travel::hotels"
        }
      }
    },
    {
      "text": "The Product runs the hotel search and lists offers",
      "kind": "product",
      "actor": "member",
      "capability": "search-hotels",
      "entities": [
        {
          "entity": "hotel-search",
          "effect": "creates",
          "facts": [
            "Destination",
            "Stay dates",
            "Rooms and guests",
            "Currency",
            "Sources",
            "Filters",
            "Owner",
            "Offers",
            "Provider errors",
            "Progress"
          ],
          "to": "Completed"
        }
      ],
      "contexts": {
        "web": {
          "place": "web::travel::hotels"
        }
      }
    },
    {
      "text": "The Member chooses Track on an offer",
      "kind": "actor",
      "actor": "member",
      "capability": "track-hotel",
      "entities": [],
      "contexts": {
        "web": {
          "place": "web::travel::hotels"
        }
      }
    },
    {
      "text": "The Product creates the hotel tracker and opens it",
      "kind": "product",
      "actor": "member",
      "capability": "track-hotel",
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
          "place": "web::travel::hotel-tracker"
        }
      }
    },
    {
      "text": "The Member sets a target price and chooses Save",
      "kind": "actor",
      "actor": "member",
      "capability": "edit-hotel-tracker",
      "entities": [],
      "contexts": {
        "web": {
          "place": "web::travel::hotel-tracker"
        }
      }
    },
    {
      "text": "The Product saves the alerts",
      "kind": "product",
      "actor": "member",
      "capability": "edit-hotel-tracker",
      "entities": [
        {
          "entity": "hotel-tracker",
          "effect": "changes",
          "facts": [
            "Target price",
            "Target armed"
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

# Search, track and set alerts

## Trigger

A Member searches a stay on Hotels.

## Outcome

The stay is tracked with the chosen alerts.
