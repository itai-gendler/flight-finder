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
      "target": "apps/web/src/app/admin/(dashboard)/users/UsersClient.tsx"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "apps/web/src/app/api/admin/users/route.ts#POST"
    }
  ]
}
---

# Add a profile

Admin adds a member profile with a username, optional display name and avatar. Quick add guest creates a generic guest profile in one step.
