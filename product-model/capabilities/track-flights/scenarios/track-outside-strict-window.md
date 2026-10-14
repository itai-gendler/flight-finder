---
{
  "kind": "validation",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Member selects a flight departing outside the window and chooses Track flights",
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
      "text": "The Product refuses with \"Selected flight does not match the strict departure window\"",
      "kind": "condition",
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

# A flight outside the strict departure window is refused

## Trigger

The request keeps only flights inside its departure window.

## Outcome

No tracker is created.
