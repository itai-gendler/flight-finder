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
      "target": "apps/web/src/components/TrackerFilters.tsx"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "apps/web/src/app/api/queries/[id]/route.ts#PATCH"
    }
  ]
}
---

# Change flight tracker filters

Change max price, max stops, max duration, airlines and departure window. Filters apply to the whole tracker group and are recorded in its edit history.
