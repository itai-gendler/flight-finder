---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Member reviews a protection option's terms, policy links and extra price and requests a fresh quote",
      "kind": "actor",
      "actor": "member",
      "entities": [
        {
          "entity": "rental-search",
          "effect": "reads",
          "as": "base",
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
      "text": "The Product queues a search for the same base rental with that protection",
      "kind": "product",
      "actor": "member",
      "entities": [
        {
          "entity": "rental-search",
          "effect": "creates",
          "as": "protected",
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
          "place": "web::travel::rental-search"
        }
      }
    }
  ]
}
---

# Quote a rental with protection

## Trigger

A completed standalone search has a verified base rental with protection options.

## Outcome

A new search checks the same rental with the chosen protection and a fresh total.

## Edge cases

- The observed extra price is never presented as a verified combined total.
