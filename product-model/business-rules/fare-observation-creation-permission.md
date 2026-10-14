---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "fare-observation",
      "effect": "creates"
    }
  ],
  "permits": [
    {
      "actors": [
        "admin"
      ],
      "when": [
        {
          "entity": "instance-settings",
          "fact": "Scraping",
          "is": "On"
        }
      ]
    },
    {
      "actors": [
        "member"
      ],
      "when": [
        {
          "entity": "instance-settings",
          "fact": "Scraping",
          "is": "On"
        }
      ]
    },
    {
      "unattended": true,
      "when": [
        {
          "entity": "instance-settings",
          "fact": "Scraping",
          "is": "On"
        }
      ]
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "apps/web/src/lib/scraper/run-scrape.ts#runScrapeAll"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "apps/web/src/app/api/queries/[id]/scrape/route.ts"
    }
  ]
}
---

# Flight prices are recorded only while scraping is on

Scheduled checks and Refresh now record fares only while Scraping is on in Extraction Config. Fares recorded with a new tracker go with its creation.

## Rationale

Pausing scraping lets the household stop background cost and requests while keeping trackers and history.
