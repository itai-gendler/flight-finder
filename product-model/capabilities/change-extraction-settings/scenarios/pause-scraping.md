---
{
  "kind": "alternative",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "Admin switches Scraping to paused",
      "kind": "actor",
      "actor": "admin",
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
          "place": "web::administration::extraction-config"
        }
      }
    },
    {
      "text": "The Product stops all background price checks",
      "kind": "product",
      "actor": "admin",
      "entities": [
        {
          "entity": "instance-settings",
          "effect": "changes",
          "facts": [
            "Scraping"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::administration::extraction-config"
        }
      }
    }
  ]
}
---

# Pause scraping

## Trigger

Admin is away or over an API quota.

## Outcome

No background checks run; trackers and price history are kept.
