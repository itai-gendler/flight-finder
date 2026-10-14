---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "notification-channel",
      "effect": "changes"
    }
  ],
  "permits": [
    {
      "actors": [
        "admin"
      ]
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "apps/web/src/app/api/admin/notifications/route.ts"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "apps/web/src/lib/admin-guard.ts#requireAdminApi"
    }
  ]
}
---

# Only Admin changes notification channels

Notification channels belong to the household and are managed in Admin → Notifications.
