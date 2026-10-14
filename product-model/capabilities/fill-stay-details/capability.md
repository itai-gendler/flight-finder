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
      "target": "apps/web/src/app/api/hotels/parse/route.ts"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "apps/web/src/lib/hotels/parse.ts#parseHotelQuery"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "apps/web/src/components/hotels/HotelSearchForm.tsx"
    }
  ]
}
---

# Fill stay details from a description

Describe a stay in plain language and let a language model fill the structured hotel form for review. The structured form works without AI.
