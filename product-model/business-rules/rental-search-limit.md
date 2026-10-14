---
{
  "appliesTo": [
    {
      "type": "capability",
      "id": "search-rental-cars"
    },
    {
      "type": "entity",
      "id": "rental-search"
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "apps/web/src/lib/cars/store.ts"
    }
  ]
}
---

# A profile runs at most three rental searches at a time

A fourth queued or running rental search is refused until one finishes or is cancelled.
