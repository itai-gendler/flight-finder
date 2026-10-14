---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Member chooses Resume tracking",
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
      "text": "The Product resumes the tracker and its group",
      "kind": "product",
      "actor": "member",
      "entities": [
        {
          "entity": "flight-tracker",
          "effect": "changes",
          "facts": [],
          "from": "Paused",
          "to": "Tracking"
        }
      ],
      "contexts": {
        "web": {
          "place": "web::travel::flights"
        }
      }
    }
  ]
}
---

# Resume tracking

## Trigger

A Member resumes a paused tracker.

## Outcome

The group shows Tracking again.
