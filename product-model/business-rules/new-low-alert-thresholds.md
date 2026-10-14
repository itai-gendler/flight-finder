---
{
  "appliesTo": [
    {
      "type": "capability",
      "id": "check-flight-prices"
    },
    {
      "type": "entity",
      "id": "instance-settings"
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "apps/web/src/lib/notifications/detect.ts#detectNewLow"
    }
  ]
}
---

# A new-low flight alert needs a drop of at least the alert thresholds

The new lowest fare must beat the last alerted low by at least the minimum drop and, when set, the minimum percentage.
