---
{
  "availability": [
    {
      "place": "web::travel"
    }
  ],
  "domain": "cars",
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "apps/web/src/app/api/cars/parse/route.ts"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "apps/web/src/lib/cars/parse.ts#parseCarQuery"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "apps/web/src/components/cars/CarNaturalLanguage.tsx"
    }
  ]
}
---

# Describe a rental

Describe a rental in plain language to get an editable draft. Location suggestions still need a catalog selection and missing driver details stay empty; nothing is searched.
