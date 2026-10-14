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
      "target": "apps/web/src/app/hotels/[id]/page.tsx"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "apps/web/src/components/hotels/HotelDetail.tsx"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "apps/web/src/app/api/hotels/[id]/route.ts#GET"
    }
  ]
}
---

# View a hotel tracker

Open a hotel tracker: stay details, price history chart and table, recent checks and errors.
