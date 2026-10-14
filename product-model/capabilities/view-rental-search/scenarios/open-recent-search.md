---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Member opens a search from Recent searches",
      "kind": "actor",
      "actor": "member",
      "entities": [
        {
          "entity": "rental-search",
          "effect": "reads",
          "facts": [
            "Pickup",
            "Return",
            "Offers",
            "Provider errors"
          ]
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

# Open a recent search

## Trigger

A Member opens a search from Recent searches.

## Outcome

Its status, offers and errors are shown.
