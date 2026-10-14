---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Member enters destination, dates, rooms and guests and chooses Search",
      "kind": "actor",
      "actor": "member",
      "entities": [],
      "contexts": {
        "web": {
          "place": "web::travel::hotels"
        }
      }
    },
    {
      "text": "The Product queues a hotel search",
      "kind": "product",
      "actor": "member",
      "entities": [
        {
          "entity": "hotel-search",
          "effect": "creates",
          "facts": [
            "Destination",
            "Stay dates",
            "Rooms and guests",
            "Currency",
            "Sources",
            "Filters",
            "Owner"
          ],
          "to": "Queued"
        }
      ],
      "contexts": {
        "web": {
          "place": "web::travel::hotels"
        }
      }
    },
    {
      "text": "The Product checks each source and stay, up to eight properties per source and stay",
      "kind": "product",
      "actor": "member",
      "entities": [
        {
          "entity": "hotel-search",
          "effect": "changes",
          "facts": [
            "Progress"
          ],
          "from": "Queued",
          "to": "Running"
        }
      ],
      "contexts": {
        "web": {
          "place": "web::travel::hotels"
        }
      }
    },
    {
      "text": "The Product keeps only offers whose taxes, occupancy and requested policies are verified",
      "kind": "product",
      "actor": "member",
      "entities": [
        {
          "entity": "hotel-search",
          "effect": "changes",
          "facts": [
            "Offers",
            "Provider errors",
            "Progress"
          ],
          "from": "Running",
          "to": "Completed"
        }
      ],
      "contexts": {
        "web": {
          "place": "web::travel::hotels"
        }
      }
    },
    {
      "text": "The Member compares offers in the list or on the map",
      "kind": "actor",
      "actor": "member",
      "entities": [
        {
          "entity": "hotel-search",
          "effect": "reads",
          "facts": [
            "Offers",
            "Provider errors"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::travel::hotels"
        }
      }
    }
  ]
}
---

# Search a stay

## Trigger

A Member fills the stay details.

## Outcome

Qualifying offers are listed with totals including taxes and fees, with any provider errors.

## Edge cases

- Hotels without verified coordinates stay in the list only; moving the map does not search again.
- Google Hotels supports one room; Booking.com supports up to four.
