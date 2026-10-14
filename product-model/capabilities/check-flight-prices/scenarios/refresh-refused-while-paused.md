---
{
  "kind": "validation",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Member chooses Refresh now",
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
      "text": "Scraping is paused, so the Product refuses with \"Scraping is paused. Resume it in the config before refreshing.\"",
      "kind": "condition",
      "entities": [
        {
          "entity": "instance-settings",
          "effect": "reads",
          "facts": [
            "Scraping"
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

# Refresh is refused while scraping is paused

## Trigger

Admin paused scraping for the instance.

## Outcome

No check runs.

## Edge cases

- A paused or expired tracker cannot be refreshed either.
