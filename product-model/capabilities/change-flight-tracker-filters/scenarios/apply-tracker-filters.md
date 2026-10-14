---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Member opens Filters, sets them and chooses Apply",
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
      "text": "The Product saves the filters on the tracker and every tracker in its group",
      "kind": "product",
      "actor": "member",
      "entities": [
        {
          "entity": "flight-tracker",
          "effect": "changes",
          "facts": [
            "Max price",
            "Max stops",
            "Max duration",
            "Preferred airlines",
            "Departure window",
            "Strict departure window"
          ]
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

# Apply filters

## Trigger

A Member narrows the fares a tracker shows.

## Outcome

The chart, best price and alerts use the new filters for every tracker in the group.
