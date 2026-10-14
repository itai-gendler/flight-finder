---
{
  "singleton": true,
  "relations": [
    {
      "entity": "passkey",
      "verb": "holds",
      "cardinality": "one-to-many"
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "apps/web/src/lib/sidedoor/access/access-store.ts#FlightFinderAccessStore"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "apps/web/src/lib/sidedoor/access/service.ts"
    }
  ]
}
---

# App access

The instance's admission: one shared password opens the app for everyone, after which each person chooses a profile.

## Information kept

- **Shared password** — the one password that opens the app, at least 12 characters
- **Owner set up** — whether the first Admin profile and shared password exist
