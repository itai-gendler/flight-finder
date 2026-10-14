---
{
  "availability": [
    {
      "place": "web::administration"
    }
  ],
  "domain": "settings",
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "apps/web/src/app/api/admin/multi-user/route.ts#POST"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "apps/web/src/lib/account-migration.ts#migrateSoloOwnership"
    }
  ]
}
---

# Enable multi-user mode

Turn on household profiles: each profile gets its own trackers and preferences; the current profile stays Admin and keeps every existing tracker.
