---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "notification-channel",
      "effect": "removes"
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

# Only Admin removes notification channels

Notification channels belong to the household and are managed in Admin → Notifications.
