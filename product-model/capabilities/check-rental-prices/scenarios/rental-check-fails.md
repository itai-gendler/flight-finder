---
{
  "kind": "edge",
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
            "Check interval"
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
      "text": "The Product runs the check",
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
      "text": "The providers fail, so the Product records the error",
      "kind": "product",
      "entities": [
        {
          "entity": "rental-search",
          "effect": "changes",
          "facts": [
            "Provider errors"
          ],
          "from": "Queued",
          "to": "Failed"
        },
        {
          "entity": "rental-tracker",
          "effect": "changes",
          "facts": [
            "Last error",
            "Last checked"
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

# A rental check fails

## Trigger

The providers cannot be read.

## Outcome

The error is shown on the tracker; no price is invented.
