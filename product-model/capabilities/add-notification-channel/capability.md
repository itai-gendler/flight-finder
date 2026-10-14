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
      "target": "apps/web/src/app/api/admin/notifications/route.ts#POST"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "apps/web/src/lib/notifications/channels/config.ts"
    }
  ]
}
---

# Add a notification channel

Add a household channel for price alerts: Telegram, email, ntfy, webhook, Pushover or a WhatsApp gateway. Secrets are stored encrypted.
