---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "member",
      "effect": "removes"
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
      "target": "apps/web/src/lib/sidedoor/access/account-management.ts#accountMutationContext"
    }
  ]
}
---

# Only Admin deletes profiles, and only with multi-user mode on

Only Admin deletes member profiles on a multi-user instance.
