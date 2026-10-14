---
{
  "availability": [
    {
      "place": "web::travel"
    }
  ],
  "domain": "hotels",
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "apps/web/src/lib/hotels/runner.ts#scheduleDueHotels"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "apps/web/src/lib/hotels/store.ts#refreshHotelTracker"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "apps/web/src/lib/hotels/alerts.ts#recordHotelAlerts"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "apps/web/src/lib/hotels/domain.ts#evaluateHotelAlerts"
    }
  ]
}
---

# Check hotel prices

Hotel trackers are checked on their interval and on demand with Refresh. A price at or below target, or a new low, raises a price alert; approximate matches alert only when allowed.
