---
{
  "availability": [
    {
      "place": "web::administration"
    }
  ],
  "domain": "users",
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "apps/web/src/app/api/admin/multi-user/route.ts#DELETE"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "apps/web/src/lib/admin-recovery.ts#disableMultiUserMode"
    }
  ]
}
---

# Disable multi-user mode

Turn household profiles off from Users, keeping the Admin credentials, setup and content.
