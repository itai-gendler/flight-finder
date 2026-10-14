---
{
  "appliesTo": [
    {
      "type": "capability",
      "id": "pause-hotel-tracker"
    },
    {
      "type": "capability",
      "id": "pause-rental-tracker"
    },
    {
      "type": "capability",
      "id": "edit-hotel-tracker"
    },
    {
      "type": "capability",
      "id": "edit-rental-tracker"
    },
    {
      "type": "entity",
      "id": "price-alert"
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

# Pausing, editing or reassigning a hotel or rental tracker withdraws its pending alerts

Alerts not yet delivered are dropped when their tracker is paused, its alert settings change or it moves to another profile; messages already sent cannot be recalled.
