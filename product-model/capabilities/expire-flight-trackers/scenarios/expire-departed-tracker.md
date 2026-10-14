---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The outbound date of a tracking flight tracker is before today",
      "kind": "condition",
      "unattended": true,
      "entities": [
        {
          "entity": "flight-tracker",
          "effect": "reads",
          "facts": [
            "Travel dates"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::travel::flight-tracker"
        }
      }
    },
    {
      "text": "The Product ends tracking for it",
      "kind": "product",
      "entities": [
        {
          "entity": "flight-tracker",
          "effect": "changes",
          "facts": [],
          "from": "Tracking",
          "to": "Expired"
        }
      ],
      "contexts": {
        "web": {
          "place": "web::travel::flight-tracker"
        }
      }
    }
  ]
}
---

# A departed trip stops being checked

## Trigger

The scheduled run starts after a tracker's outbound date.

## Outcome

The tracker shows Expired and is no longer checked.
