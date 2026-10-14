---
{
  "availability": [
    {
      "place": "web::travel"
    }
  ],
  "domain": "flights",
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "apps/web/src/lib/scraper/expire-queries.ts#expireDepartedQueries"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "apps/web/src/lib/cron.ts"
    }
  ]
}
---

# End tracking after departure

Once a trip's departure day has passed, its tracker stops being checked.
