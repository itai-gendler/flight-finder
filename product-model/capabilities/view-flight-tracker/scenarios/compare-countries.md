---
{
  "kind": "alternative",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Member switches the view to Country comparison",
      "kind": "actor",
      "actor": "member",
      "entities": [
        {
          "entity": "fare-observation",
          "effect": "reads",
          "facts": [
            "Country",
            "Price"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::travel::flight-tracker"
        }
      }
    },
    {
      "text": "Until the first comparison check runs, the Product notes that country prices are pending",
      "kind": "condition",
      "entities": [
        {
          "entity": "flight-tracker",
          "effect": "reads",
          "facts": [
            "Comparison countries"
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

# Compare prices by country

## Trigger

The tracker compares prices from other countries.

## Outcome

Prices are shown per country, including the local baseline.
