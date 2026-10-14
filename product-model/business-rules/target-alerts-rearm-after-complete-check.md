---
{
  "appliesTo": [
    {
      "type": "capability",
      "id": "check-hotel-prices"
    },
    {
      "type": "capability",
      "id": "check-rental-prices"
    },
    {
      "type": "entity",
      "id": "price-alert"
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "apps/web/src/lib/hotels/domain.ts#evaluateHotelAlerts"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "apps/web/src/lib/cars/alerts.ts#evaluateCarAlerts"
    }
  ]
}
---

# A target alert fires once until a complete check above the target re-arms it

Reaching the target alerts once; the target re-arms only after a complete, valid check above it, or when the target changes.
