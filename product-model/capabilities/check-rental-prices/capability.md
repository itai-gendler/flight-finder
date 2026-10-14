---
{
  "availability": [
    {
      "place": "web::travel"
    }
  ],
  "domain": "cars",
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "apps/web/src/lib/travel/schedule.ts"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "apps/web/src/lib/cars/store.ts#refreshCarTracker"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "apps/web/src/lib/cars/alerts.ts#evaluateCarAlerts"
    }
  ]
}
---

# Check rental prices

Rental trackers are checked on their interval and on demand with Check saved rental prices. Only verified prices can alert.
