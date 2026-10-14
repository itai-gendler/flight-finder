---
{
  "kind": "validation",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Member sets Max stops to 11 and chooses Apply",
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
      "text": "The Product refuses with \"Max stops must be a whole number from 0 to 10.\"",
      "kind": "condition",
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

# Out-of-range filters are refused

## Trigger

A Member enters an invalid filter.

## Outcome

Nothing changes.

## Edge cases

- A concurrent group or ownership change is refused with a request to reload.
