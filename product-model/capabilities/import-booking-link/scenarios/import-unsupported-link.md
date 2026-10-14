---
{
  "kind": "validation",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Member pastes a link on Cars",
      "kind": "actor",
      "actor": "member",
      "entities": [],
      "contexts": {
        "web": {
          "place": "web::travel::cars"
        }
      }
    },
    {
      "text": "The link is not a supported rental link, so the Product refuses with \"Could not import this link\"",
      "kind": "condition",
      "entities": [],
      "contexts": {
        "web": {
          "place": "web::travel::cars"
        }
      }
    }
  ]
}
---

# An unsupported link is refused

## Trigger

A Member pastes a link the Product cannot read.

## Outcome

Nothing is filled; the reason is shown.
