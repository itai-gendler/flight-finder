---
{
  "appliesTo": [
    {
      "type": "capability",
      "id": "expire-flight-trackers"
    },
    {
      "type": "entity",
      "id": "flight-tracker"
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "apps/web/src/lib/scraper/expire-queries.ts#expireDepartedQueries"
    }
  ]
}
---

# Flight tracking ends once the departure day has passed

A tracker whose outbound date is before today is no longer checked.

## Rationale

A trip is unbookable once its outbound date has passed.
