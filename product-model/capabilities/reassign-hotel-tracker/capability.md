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
      "target": "apps/web/src/components/hotels/HotelDetail.tsx"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "apps/web/src/lib/hotels/store.ts#editHotelTracker"
    }
  ]
}
---

# Reassign a hotel tracker

Admin moves a hotel tracker to another profile on a multi-user instance.
