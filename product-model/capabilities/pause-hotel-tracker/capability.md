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
      "target": "apps/web/src/components/hotels/HotelDetail.tsx"
    }
  ]
}
---

# Pause a hotel tracker

Stop checks and pending alerts for a hotel tracker.
