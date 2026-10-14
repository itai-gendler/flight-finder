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
      "target": "apps/web/src/components/AggregatorPicker.tsx"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "apps/web/src/lib/scraper/run-scrape.ts#resolveAggregatorChain"
    }
  ]
}
---

# Change a flight tracker's price sources

Choose and order the price sources this tracker uses, among the sources Admin allows.
