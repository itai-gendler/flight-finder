---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Member opens Cars",
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
      "text": "The Product lists the Member's own rental trackers",
      "kind": "product",
      "actor": "member",
      "entities": [
        {
          "entity": "rental-tracker",
          "effect": "reads",
          "facts": [
            "Label",
            "Latest price",
            "Last error"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::travel::cars"
        }
      }
    }
  ]
}
---

# Browse rental trackers

## Trigger

A Member opens Cars.

## Outcome

The profile's rental trackers are listed.
