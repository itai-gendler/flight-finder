---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "rental-tracker",
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
      "target": "apps/web/src/lib/cars/store.ts#editCarTracker"
    }
  ]
}
---

# Only Admin reassigns a rental tracker, and only with multi-user mode on

Moving a rental tracker to another profile is an Admin action that exists only for household profiles.
