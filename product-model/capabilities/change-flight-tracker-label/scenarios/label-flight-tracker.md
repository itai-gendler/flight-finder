---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Member chooses + Add label and types a label",
      "kind": "actor",
      "actor": "member",
      "entities": [],
      "contexts": {
        "web": {
          "place": "web::travel::flight-tracker"
        }
      }
    },
    {
      "text": "The Product saves the label",
      "kind": "product",
      "actor": "member",
      "entities": [
        {
          "entity": "flight-tracker",
          "effect": "changes",
          "facts": [
            "Label"
          ]
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

# Label a tracker

## Trigger

A Member owns the tracker.

## Outcome

The label is shown on the chart and in lists.
