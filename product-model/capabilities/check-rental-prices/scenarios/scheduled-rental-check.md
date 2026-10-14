---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "A tracking rental tracker is due",
      "kind": "condition",
      "unattended": true,
      "entities": [
        {
          "entity": "rental-tracker",
          "effect": "reads",
          "facts": [
            "Check interval",
            "Last checked"
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
      "text": "The Product runs a rental search for the tracked rental",
      "kind": "product",
      "entities": [
        {
          "entity": "rental-search",
          "effect": "creates",
          "facts": [
            "Pickup",
            "Return",
            "Pickup time",
            "Return time",
            "Driver age",
            "Residence country",
            "Licence years",
            "Providers",
            "Requested extras",
            "Currency",
            "Owner"
          ],
          "to": "Queued"
        }
      ],
      "contexts": {
        "web": {
          "place": "web::travel::rental-tracker"
        }
      }
    },
    {
      "text": "The Product records the price evidence",
      "kind": "product",
      "entities": [
        {
          "entity": "rental-search",
          "effect": "changes",
          "facts": [
            "Offers",
            "Unverified candidates",
            "Provider errors",
            "Offers checked"
          ],
          "from": "Queued",
          "to": "Completed"
        },
        {
          "entity": "rental-price-observation",
          "effect": "creates",
          "facts": [
            "Provider",
            "Rental total",
            "Currency",
            "Payment timing",
            "Deposit",
            "Excess",
            "Fuel and mileage",
            "Driver requirements",
            "Extras",
            "Eligible",
            "Reasons",
            "Observed at",
            "Contract"
          ]
        },
        {
          "entity": "rental-tracker",
          "effect": "changes",
          "facts": [
            "Latest price",
            "Historical low",
            "Target armed",
            "Last checked"
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
      "text": "The verified total is a new low, so the Product raises an alert",
      "kind": "product",
      "entities": [
        {
          "entity": "price-alert",
          "effect": "creates",
          "facts": [
            "Message",
            "Recipients"
          ],
          "to": "Pending"
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

# Scheduled check finds a new low

## Trigger

A tracking rental tracker is due.

## Outcome

The verified price is in the history and a new-low alert waits for delivery.
