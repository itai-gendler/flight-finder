---
{
  "availability": [
    {
      "place": "web::administration"
    }
  ],
  "domain": "notifications",
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "apps/web/src/app/admin/(dashboard)/notifications/page.tsx"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "apps/web/src/app/api/admin/config/route.ts"
    }
  ]
}
---

# Change alert thresholds

Set the minimum absolute and percentage drop for new-low flight alerts and the public site URL used for links in alerts.
