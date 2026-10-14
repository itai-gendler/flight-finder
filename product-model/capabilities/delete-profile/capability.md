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
      "target": "apps/web/src/app/api/admin/users/[id]/route.ts#DELETE"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "apps/web/src/lib/sidedoor/access/access-store.ts#FlightFinderAccessStore"
    }
  ]
}
---

# Delete a profile

Admin deletes a member profile. Its trackers and their history are kept without an owner.
