---
{
  "kind": "alternative",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Member chooses Check saved rental prices",
      "kind": "actor",
      "actor": "member",
      "entities": [
        {
          "entity": "rental-tracker",
          "effect": "reads",
          "facts": [
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
      "text": "The Product queues a check, reusing one already running",
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
          "place": "web::travel::rental-tracker"
        }
      }
    }
  ]
}
---

# Check saved rental prices

## Trigger

A Member wants a current price.

## Outcome

A check runs for the revision the Member saw.

## Edge cases

- After a lost acknowledgement the saved request is recovered rather than started again.
