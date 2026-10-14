---
{
  "kind": "validation",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Member chooses Room mode and Track on that offer",
      "kind": "actor",
      "actor": "member",
      "entities": [],
      "contexts": {
        "web": {
          "place": "web::travel::hotels"
        }
      }
    },
    {
      "text": "The Product refuses with \"This source did not provide a room identity; choose best matching offer\"",
      "kind": "condition",
      "entities": [],
      "contexts": {
        "web": {
          "place": "web::travel::hotels"
        }
      }
    }
  ]
}
---

# A room cannot be tracked without a room identity

## Trigger

The source did not give the offer a room name.

## Outcome

No tracker is created.
