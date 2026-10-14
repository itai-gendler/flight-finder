---
{
  "domain": "notifications",
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "apps/web/src/app/api/admin/notifications/route.ts"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "apps/web/src/lib/notifications/channels/config.ts"
    }
  ]
}
---

# Notification channel

A household destination for price alerts: Telegram, email, ntfy, webhook, Pushover or a WhatsApp gateway.

## Information kept

- **Type** — telegram, email, ntfy, webhook, Pushover or WhatsApp
- **Label** — an optional friendly name
- **Settings** — the destination settings of its type, such as chat, topic, address, devices or priority
- **Secret credentials** — tokens, passwords and keys, stored encrypted and never shown again

## States

### Enabled

Receives alerts.

### Disabled

Skipped until enabled.
