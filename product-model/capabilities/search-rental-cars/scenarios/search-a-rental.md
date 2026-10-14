---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Member chooses catalog locations, dates, times, driver age, residence and licence years, providers, and starts the search",
      "kind": "actor",
      "actor": "member",
      "entities": [],
      "contexts": {
        "web": {
          "place": "web::travel::cars"
        }
      }
    },
    {
      "text": "The Product queues a rental search",
      "kind": "product",
      "actor": "member",
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
          "place": "web::travel::cars"
        }
      }
    },
    {
      "text": "The Product checks up to eight offers per provider in headless browsers",
      "kind": "product",
      "actor": "member",
      "entities": [
        {
          "entity": "rental-search",
          "effect": "changes",
          "facts": [],
          "from": "Queued",
          "to": "Running"
        }
      ],
      "contexts": {
        "web": {
          "place": "web::travel::rental-search"
        }
      }
    },
    {
      "text": "The Product records verified offers apart from candidates whose price it cannot verify",
      "kind": "product",
      "actor": "member",
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
          "from": "Running",
          "to": "Completed"
        }
      ],
      "contexts": {
        "web": {
          "place": "web::travel::rental-search"
        }
      }
    },
    {
      "text": "The Member reviews totals, payment timing, deposit, excess and policies",
      "kind": "actor",
      "actor": "member",
      "entities": [
        {
          "entity": "rental-search",
          "effect": "reads",
          "facts": [
            "Offers",
            "Unverified candidates",
            "Provider errors",
            "Offers checked"
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

# Search a rental

## Trigger

A Member fills the rental form.

## Outcome

The search page shows offers checked, verified totals with their terms, unverified candidates and errors.

## Edge cases

- DiscoverCars cannot search an exact age from 30 to 65 except 35, or above 80; Auto Europe can.
- Requested extras need supported pricing; an unknown charge is never treated as free.
