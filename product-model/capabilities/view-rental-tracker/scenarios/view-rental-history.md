---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Member opens the rental tracker",
      "kind": "actor",
      "actor": "member",
      "entities": [
        {
          "entity": "rental-tracker",
          "effect": "reads",
          "facts": [
            "Label",
            "Rental criteria",
            "Tracking mode",
            "Latest price",
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
      "text": "The Member reads the price evidence",
      "kind": "actor",
      "actor": "member",
      "entities": [
        {
          "entity": "rental-price-observation",
          "effect": "reads",
          "facts": [
            "Rental total",
            "Payment timing",
            "Deposit",
            "Excess",
            "Eligible"
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
      "text": "The Member reads the alert delivery status",
      "kind": "actor",
      "actor": "member",
      "entities": [
        {
          "entity": "price-alert",
          "effect": "reads",
          "facts": [
            "Delivered channels",
            "Last error"
          ]
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

# View rental price history

## Trigger

A Member opens a rental tracker.

## Outcome

Price evidence, checks and alert delivery are shown.
