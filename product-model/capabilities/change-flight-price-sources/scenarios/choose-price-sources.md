---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Member turns on Skyscanner in Sources",
      "kind": "actor",
      "actor": "member",
      "entities": [
        {
          "entity": "instance-settings",
          "effect": "reads",
          "facts": [
            "Allowed price sources"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::travel::flight-tracker"
        }
      }
    },
    {
      "text": "The Product saves the tracker's sources",
      "kind": "product",
      "actor": "member",
      "entities": [
        {
          "entity": "flight-tracker",
          "effect": "changes",
          "facts": [
            "Price sources"
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

# Choose price sources

## Trigger

A Member wants this tracker to try another source.

## Outcome

Later checks walk the chosen sources in order.

## Edge cases

- Sources Admin disabled show "Disabled by admin" and cannot be chosen.
