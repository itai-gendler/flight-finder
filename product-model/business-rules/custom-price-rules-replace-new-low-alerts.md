---
{
  "appliesTo": [
    {
      "type": "capability",
      "id": "check-flight-prices"
    },
    {
      "type": "entity",
      "id": "price-rule"
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "apps/web/src/lib/notifications/flights.ts#recordFlightAlertInTransaction"
    }
  ]
}
---

# Enabled price rules replace historical-low alerts for their tracker

A flight tracker with an enabled custom rule alerts only through its rules; without one, it alerts on historical lows.
