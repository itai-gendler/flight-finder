---
{
  "appliesTo": [
    {
      "type": "capability",
      "id": "change-flight-tracker-filters"
    },
    {
      "type": "entity",
      "id": "tracker-edit"
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "apps/web/src/app/api/queries/[id]/route.ts#PATCH"
    }
  ]
}
---

# Every filter change on a flight tracker is recorded in its edit history

Each change to max price, stops, duration, airlines or departure window adds an entry naming the before and after values; the chart shows it as a marker.
