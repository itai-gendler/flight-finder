---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "price-alert",
      "effect": "changes",
      "to": "Withdrawn"
    }
  ],
  "permits": [
    {
      "actors": [
        "admin"
      ]
    },
    {
      "related": [
        {
          "verb": "raises",
          "entity": "hotel-tracker"
        },
        {
          "verb": "owns",
          "entity": "member"
        }
      ]
    },
    {
      "related": [
        {
          "verb": "raises",
          "entity": "rental-tracker"
        },
        {
          "verb": "owns",
          "entity": "member"
        }
      ]
    },
    {
      "related": [
        {
          "verb": "has",
          "entity": "flight-tracker"
        },
        {
          "verb": "owns",
          "entity": "member"
        }
      ]
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "apps/web/src/lib/hotels/store.ts#editHotelTracker"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "apps/web/src/lib/cars/store.ts#editCarTracker"
    }
  ]
}
---

# Only Admin or the tracker's owner withdraws a pending price alert

Pending alerts are withdrawn when Admin or the owning member pauses, edits or reassigns the tracker, or when Admin turns on multi-user mode.
