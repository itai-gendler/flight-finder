---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Member chooses Resume",
      "kind": "actor",
      "actor": "member",
      "entities": [],
      "contexts": {
        "web": {
          "place": "web::travel::hotel-tracker"
        }
      }
    },
    {
      "text": "The Product resumes the tracker and makes it due now",
      "kind": "product",
      "actor": "member",
      "entities": [
        {
          "entity": "hotel-tracker",
          "effect": "changes",
          "facts": [],
          "from": "Paused",
          "to": "Tracking"
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

# Resume a hotel tracker

## Trigger

A Member resumes a paused tracker.

## Outcome

The tracker is checked again right away.
