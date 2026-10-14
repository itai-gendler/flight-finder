---
{
  "kind": "validation",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Member requests protection for an unverified rental",
      "kind": "actor",
      "actor": "member",
      "entities": [],
      "contexts": {
        "web": {
          "place": "web::travel::rental-search"
        }
      }
    },
    {
      "text": "The Product refuses: protection review requires a verified base rental and itemized selected options",
      "kind": "condition",
      "entities": [
        {
          "entity": "rental-search",
          "effect": "reads",
          "facts": [
            "Offers"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::travel::rental-search"
        }
      }
    }
  ]
}
---

# Protection needs a verified base rental

## Trigger

The base rental or its options are not verified.

## Outcome

No quote is requested.
