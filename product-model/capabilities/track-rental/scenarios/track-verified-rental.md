---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Member chooses best or contract mode, a target and an interval, and tracks the offer",
      "kind": "actor",
      "actor": "member",
      "entities": [
        {
          "entity": "rental-search",
          "effect": "reads",
          "as": "searched",
          "facts": [
            "Offers"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::travel::rental-search"
        }
      }
    },
    {
      "text": "The Product creates the rental tracker and queues its first check",
      "kind": "product",
      "actor": "member",
      "entities": [
        {
          "entity": "rental-tracker",
          "effect": "creates",
          "facts": [
            "Label",
            "Rental criteria",
            "Tracking mode",
            "Selected contract",
            "Currency",
            "Target price",
            "New-low alerts",
            "Check interval",
            "Revision",
            "Target armed",
            "Owner"
          ],
          "to": "Tracking"
        },
        {
          "entity": "rental-search",
          "effect": "creates",
          "as": "first-check",
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
          "to": "Queued",
          "with": "rental-tracker"
        }
      ],
      "contexts": {
        "web": {
          "place": "web::travel::rental-search"
        }
      }
    }
  ]
}
---

# Track a verified rental

## Trigger

A completed search shows a verified offer.

## Outcome

A rental tracker exists and its first check is queued; the page links to it.
