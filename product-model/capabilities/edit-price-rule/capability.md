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
      "target": "apps/web/src/components/notifications/TrackerPriceRules.tsx"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "apps/web/src/lib/notifications/rules/store.ts#updatePriceRules"
    }
  ]
}
---

# Edit a price rule

Change a rule's scope, thresholds, cooldown or whether it is enabled.
