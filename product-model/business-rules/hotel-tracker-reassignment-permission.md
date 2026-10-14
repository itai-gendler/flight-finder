---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "hotel-tracker",
      "effect": "changes",
      "facts": [
        "Owner"
      ]
    }
  ],
  "permits": [
    {
      "actors": [
        "admin"
      ],
      "when": [
        {
          "entity": "instance-settings",
          "fact": "Multi-user mode",
          "is": "On"
        }
      ]
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "apps/web/src/lib/hotels/store.ts#editHotelTracker"
    }
  ]
}
---

# Only Admin reassigns a hotel tracker, and only with multi-user mode on

Moving a hotel tracker to another profile is an Admin action that exists only for household profiles.
