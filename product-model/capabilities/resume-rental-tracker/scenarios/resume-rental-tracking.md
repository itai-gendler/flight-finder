---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Member chooses Resume and confirms",
      "kind": "actor",
      "actor": "member",
      "entities": [],
      "contexts": {
        "web": {
          "place": "web::travel::rental-tracker"
        }
      }
    },
    {
      "text": "The Product resumes the tracker",
      "kind": "product",
      "actor": "member",
      "entities": [
        {
          "entity": "rental-tracker",
          "effect": "changes",
          "facts": [
            "Revision"
          ],
          "from": "Paused",
          "to": "Tracking"
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

# Resume a rental tracker

## Trigger

A Member resumes a paused tracker.

## Outcome

The tracker is due for a check right away.
