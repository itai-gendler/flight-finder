---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Member describes the stay and chooses Fill details",
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
      "text": "The Product asks the configured language model to fill destination, dates, rooms, currency and filters",
      "kind": "product",
      "actor": "member",
      "entities": [],
      "contexts": {
        "web": {
          "place": "web::travel::hotels"
        }
      }
    },
    {
      "text": "The filled details are shown for review",
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

# Fill details

## Trigger

A Member describes a stay.

## Outcome

The form is filled for review; nothing is searched yet.

## Edge cases

- Descriptions must be 1 to 2000 characters.
