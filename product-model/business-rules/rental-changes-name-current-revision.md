---
{
  "appliesTo": [
    {
      "type": "capability",
      "id": "edit-rental-tracker"
    },
    {
      "type": "capability",
      "id": "check-rental-prices"
    },
    {
      "type": "capability",
      "id": "delete-rental-tracker"
    },
    {
      "type": "entity",
      "id": "rental-tracker"
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "apps/web/src/lib/cars/store.ts"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "apps/web/src/app/api/cars/[id]/route.ts"
    }
  ]
}
---

# Changes to a rental tracker must name its current revision

Edits, checks and deletion carry the revision last read; a stale revision is refused and the current settings are shown without claiming the earlier request succeeded.
