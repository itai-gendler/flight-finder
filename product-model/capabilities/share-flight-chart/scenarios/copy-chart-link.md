---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Member chooses Copy shareable link",
      "kind": "actor",
      "actor": "member",
      "entities": [
        {
          "entity": "flight-tracker",
          "effect": "reads",
          "facts": []
        }
      ],
      "contexts": {
        "web": {
          "place": "web::travel::flight-tracker"
        }
      }
    },
    {
      "text": "The Product copies the chart address and shows Copied!",
      "kind": "product",
      "actor": "member",
      "entities": [],
      "contexts": {
        "web": {
          "place": "web::travel::flight-tracker"
        }
      }
    }
  ]
}
---

# Copy the shareable link

## Trigger

A Member wants to share a chart.

## Outcome

The chart link is copied.

## Edge cases

- Download CSV saves the shown price history.
