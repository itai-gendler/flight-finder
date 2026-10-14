---
{
  "availability": [
    {
      "place": "web::travel"
    }
  ],
  "domain": "flights",
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "apps/web/src/components/notifications/TrackerNotifications.tsx"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "apps/web/src/lib/notifications/subscriptions/policy.ts#updateNotificationSettings"
    }
  ]
}
---

# Choose flight alert recipients

Choose whether a tracker's alerts go to the household defaults or to chosen notification channels. Choosing no channels mutes the tracker.
