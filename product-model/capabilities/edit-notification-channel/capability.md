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
      "target": "apps/web/src/app/api/admin/notifications/[id]/route.ts#PATCH"
    }
  ]
}
---

# Edit a notification channel

Change a channel's label and settings. Leaving a secret field blank keeps the saved value.
