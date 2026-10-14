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
      "target": "apps/web/src/app/api/parse/route.ts"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "apps/web/src/lib/scraper/parse-query.ts#parseFlightQuery"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "apps/web/src/components/SearchBar.tsx"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "apps/web/src/components/ClarificationCard.tsx"
    }
  ]
}
---

# Describe a flight

Type a trip in plain language, such as "NYC to Paris around June 15 +/- 3 days". A language model turns it into a reviewable request and asks follow-up questions when it is unsure.
