---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Member pastes a selected flight link on Flights",
      "kind": "actor",
      "actor": "member",
      "entities": [],
      "contexts": {
        "web": {
          "place": "web::travel::flights"
        }
      }
    },
    {
      "text": "The Product decodes the route, dates, cabin and trip type and fills the request",
      "kind": "product",
      "actor": "member",
      "entities": [],
      "contexts": {
        "web": {
          "place": "web::travel::flights"
        }
      }
    }
  ]
}
---

# Import a flight link

## Trigger

A Member has a selected itinerary link from Google Flights.

## Outcome

The flight request is filled from the link for review; tracking the import follows exactly that itinerary.
