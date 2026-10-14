---
{
  "availability": [
    {
      "place": "web::travel"
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "apps/web/src/components/hotels/HotelMapPreferences.tsx"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "apps/web/src/app/api/account/settings/route.ts"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "apps/web/src/lib/hotels/map-config.ts#validateHotelMapPreferences"
    }
  ]
}
---

# Change map preferences

Choose the hotel map style or turn the map off, from the map preferences panel or Account settings. Saving a preference does not open the map.
