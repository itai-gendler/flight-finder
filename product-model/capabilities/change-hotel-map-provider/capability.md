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
      "target": "apps/web/src/components/hotels/HotelMapAdmin.tsx"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "apps/web/src/app/api/admin/hotel-map/route.ts"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "apps/web/src/lib/hotels/map-config.ts#validateHotelMapConfig"
    }
  ]
}
---

# Change the hotel map provider

Choose OpenFreeMap or a custom public HTTPS MapLibre style with its resource origins and privacy and attribution links, or turn maps off. Saving does not contact the provider.
