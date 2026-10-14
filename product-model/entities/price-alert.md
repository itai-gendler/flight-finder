---
{
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "apps/web/prisma/schema.prisma"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "apps/web/src/lib/notifications/delivery.ts#deliverClaimedAlert"
    }
  ]
}
---

# Price alert

A price event waiting to be delivered to notification channels: a new low, a reached target or a price rule. Delivery retries until a channel accepts it.

## Information kept

- **Message** — the title, text and tracker link
- **Recipients** — the household channels or the tracker's chosen channels
- **Delivered channels** — channels that accepted it
- **Last error** — why delivery has not completed
- **Next attempt** — when delivery is retried

## States

### Pending

Waiting for delivery.

### Delivered

Accepted by its channels.

### Withdrawn

Dropped because its tracker was paused, changed or reassigned.
