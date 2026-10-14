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
      "target": "apps/web/src/app/api/preview/route.ts"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "apps/web/src/app/api/preview/[id]/route.ts"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "apps/web/src/components/ConfirmationCard.tsx"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "apps/web/src/components/ManualEntryForm.tsx"
    }
  ]
}
---

# Show available flights

Look up current fares for a reviewed request (or details entered manually) before tracking. Each route, destination and date pair is a separate lookup.
