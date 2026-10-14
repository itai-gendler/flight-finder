---
{
  "availability": [
    {
      "place": "web::travel"
    },
    {
      "place": "web::administration"
    }
  ],
  "domain": "flights",
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "apps/web/src/components/DeleteTracker.tsx"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "apps/web/src/app/api/queries/[id]/route.ts#DELETE"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "apps/web/src/app/api/admin/queries/[id]/route.ts"
    }
  ]
}
---

# Delete a flight tracker

Stop tracking permanently: the tracker and all its price history are deleted.
