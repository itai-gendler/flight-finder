---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "instance-settings",
      "effect": "changes"
    }
  ],
  "permits": [
    {
      "actors": [
        "admin"
      ]
    },
    {
      "actors": [
        "instance-operator"
      ]
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "apps/web/src/middleware.ts"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "apps/web/src/app/api/admin/config/route.ts"
    }
  ]
}
---

# Only Admin changes instance settings

Settings, Extraction Config, alert thresholds, setup and multi-user mode are Admin's. The Instance operator sets the login address from a terminal on the server.
