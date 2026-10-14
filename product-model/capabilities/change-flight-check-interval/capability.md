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
      "target": "apps/web/src/components/ScrapeInterval.tsx"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "apps/web/src/app/admin/(dashboard)/queries/QueryRow.tsx"
    }
  ]
}
---

# Change how often a flight tracker is checked

Choose Check every 1, 3, 6, 12 or 24 hours, or Auto to follow the instance default.
