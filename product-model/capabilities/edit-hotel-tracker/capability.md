---
{
  "availability": [
    {
      "place": "web::travel"
    }
  ],
  "domain": "hotels",
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "apps/web/src/lib/hotels/store.ts#editHotelTracker"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "apps/web/src/components/hotels/HotelOptions.tsx"
    }
  ]
}
---

# Edit hotel tracker alerts

Change a hotel tracker's target price, new-low alerts, approximate-match alerts and check interval. Stay criteria cannot change; create a new tracker instead.
