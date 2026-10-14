---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "member",
      "effect": "creates"
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

# Only Admin adds profiles, and only with multi-user mode on

Member profiles exist only on a multi-user instance and only Admin adds them.
