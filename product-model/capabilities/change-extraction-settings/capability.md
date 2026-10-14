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
      "target": "apps/web/src/app/admin/(dashboard)/config/page.tsx"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "apps/web/src/app/api/admin/config/route.ts"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "apps/web/src/lib/cron.ts#updateCronInterval"
    }
  ]
}
---

# Change extraction settings

Change the AI provider, model, credentials, default check interval, currency and country, search method, allowed price sources, limits and rate caps, and pause or resume scraping.
