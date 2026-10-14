---
{
  "appliesTo": [
    {
      "type": "capability",
      "id": "check-hotel-prices"
    },
    {
      "type": "entity",
      "id": "hotel-tracker"
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "apps/web/src/lib/hotels/domain.ts#matchHotelSelection"
    }
  ]
}
---

# Approximate room and rate matches alert only when the tracker allows them

In room mode an offer that only approximately matches the chosen room and rate is recorded but alerts only with Approximate alerts on.
