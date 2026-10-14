---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "passkey",
      "effect": "removes"
    }
  ],
  "permits": [
    {
      "actors": [
        "admin"
      ]
    },
    {
      "actors": [
        "instance-operator"
      ]
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "apps/web/src/app/access/security/SecurityScreen.tsx"
    }
  ]
}
---

# Only Admin removes passkeys, or a password change removes them all

Admin removes passkeys in Account security; changing or resetting the shared password removes every passkey.
