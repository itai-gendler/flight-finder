---
{
  "availability": [
    {
      "place": "web::travel"
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "apps/web/src/app/api/travel/import/route.ts"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "apps/web/src/lib/travel/import-draft.ts#importTravelDraft"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "apps/web/src/components/travel/LinkImport.tsx"
    }
  ]
}
---

# Import a booking link

Paste a Google Flights, hotel or rental link to fill a search for review. Importing decodes the link only; it starts no provider search, AI call or tracker.
