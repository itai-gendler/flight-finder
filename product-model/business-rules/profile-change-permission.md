---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "profile",
      "effect": "changes"
    }
  ],
  "permits": [
    {
      "related": [
        {
          "verb": "has",
          "entity": "member"
        }
      ],
      "when": [
        {
          "entity": "instance-settings",
          "fact": "Multi-user mode",
          "is": "On"
        }
      ]
    },
    {
      "related": [
        {
          "verb": "has",
          "entity": "admin"
        }
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
      "target": "apps/web/src/app/api/account/settings/route.ts"
    }
  ]
}
---

# A profile's settings are changed only by its own holder, with multi-user mode on

Account settings and saved map preferences belong to the profile that is in use; they exist on multi-user instances.
