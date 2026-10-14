---
{
  "availability": [
    {
      "place": "web::travel"
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "apps/web/src/lib/travel/schedule.ts"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "apps/web/src/lib/notifications/delivery.ts#deliverClaimedAlert"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "apps/web/src/lib/notifications/flights.ts"
    }
  ]
}
---

# Deliver price alerts

Pending price alerts are delivered to their channels in the background, retried every five minutes until accepted. Channels that accepted are not sent again.
