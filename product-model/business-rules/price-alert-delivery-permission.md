---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "price-alert",
      "effect": "changes",
      "to": "Delivered"
    }
  ],
  "permits": [
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
      "target": "apps/web/src/lib/travel/schedule.ts"
    }
  ]
}
---

# Price alerts are delivered only while scraping is on

Pending price alerts wait while Scraping is paused and are delivered once it is on again.
