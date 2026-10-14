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
      "target": "apps/web/src/components/SavedTrackers.tsx"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "apps/web/src/app/admin/(dashboard)/queries/QueryRow.tsx"
    }
  ]
}
---

# Pause a flight tracker

Stop checking a tracker group until it is resumed.
