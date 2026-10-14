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

# Add a price rule

Add a custom alert rule to a flight tracker: a target price, an absolute drop or a percentage drop, with an optional cooldown. Enabled rules replace historical-low alerts for that tracker.
