---
{
  "appliesTo": [
    {
      "type": "capability",
      "id": "track-rental"
    },
    {
      "type": "capability",
      "id": "check-rental-prices"
    },
    {
      "type": "entity",
      "id": "rental-price-observation"
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "apps/web/src/lib/cars/pricing.ts#assessCarPrice"
    }
  ]
}
---

# Only verified rental prices start tracking or alert

An offer whose total, charges or requested extras cannot be established stays visible for inspection but cannot be tracked or trigger an alert.
