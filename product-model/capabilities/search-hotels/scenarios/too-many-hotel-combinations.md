---
{
  "kind": "validation",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Member chooses a long window with both sources and chooses Search",
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
      "text": "The Product refuses with \"Search exceeds 24 date/source combinations; narrow dates or choose one source\"",
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

# Too many date and source combinations are refused

## Trigger

A flexible window would need more than 24 date and source combinations.

## Outcome

Nothing is searched.
