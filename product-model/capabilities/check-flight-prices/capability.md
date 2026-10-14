---
{
  "availability": [
    {
      "place": "web::travel"
    },
    {
      "place": "web::administration"
    }
  ],
  "domain": "flights",
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "apps/web/src/lib/cron.ts"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "apps/web/src/lib/scraper/run-scrape.ts#runScrapeAll"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "apps/web/src/app/api/queries/[id]/scrape/route.ts"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "apps/web/src/lib/notifications/flights.ts#recordFlightAlertInTransaction"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "apps/web/src/lib/notifications/detect.ts#detectNewLow"
    }
  ]
}
---

# Check flight prices

Flight prices are checked on each tracker's interval and on demand with Refresh now. Each check walks the tracker's price sources, records new fares and, when the price drops enough or a price rule fires, raises a price alert.
