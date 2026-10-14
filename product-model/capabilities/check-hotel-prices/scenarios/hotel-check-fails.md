---
{
  "kind": "edge",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "A tracking hotel tracker is due",
      "kind": "condition",
      "unattended": true,
      "entities": [
        {
          "entity": "hotel-tracker",
          "effect": "reads",
          "facts": [
            "Check interval"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::travel::hotel-tracker"
        }
      }
    },
    {
      "text": "The Product runs the check",
      "kind": "product",
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
          "place": "web::travel::hotel-tracker"
        }
      }
    },
    {
      "text": "The sources fail, so the Product records the error",
      "kind": "product",
      "entities": [
        {
          "entity": "hotel-search",
          "effect": "changes",
          "facts": [
            "Provider errors"
          ],
          "from": "Queued",
          "to": "Failed"
        },
        {
          "entity": "hotel-tracker",
          "effect": "changes",
          "facts": [
            "Last error",
            "Last checked"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::travel::hotel-tracker"
        }
      }
    }
  ]
}
---

# A check fails

## Trigger

The sources cannot be read.

## Outcome

The error is shown on the tracker; no price is invented.
