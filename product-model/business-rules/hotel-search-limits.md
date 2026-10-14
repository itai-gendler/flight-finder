---
{
  "appliesTo": [
    {
      "type": "capability",
      "id": "search-hotels"
    },
    {
      "type": "entity",
      "id": "hotel-search"
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "apps/web/src/lib/hotels/domain.ts#expandHotelStays"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "apps/web/src/lib/hotels/store.ts#createHotelSearch"
    }
  ]
}
---

# A hotel search covers at most 24 date and source combinations, three per profile at a time

Flexible dates expand into stays; with both sources they count twice. A profile may have three hotel searches queued or running.
