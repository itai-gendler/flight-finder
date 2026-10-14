---
{
  "availability": [
    {
      "place": "web::administration"
    }
  ],
  "domain": "settings",
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "apps/web/src/app/settings/page.tsx"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "apps/web/src/lib/community-sync.ts"
    }
  ]
}
---

# Change community data sharing

Opt in or out of sharing anonymized fares (route, date, price, airline, stops, cabin, time) with the community dataset, and choose whether this instance accepts community registrations as a hub.
