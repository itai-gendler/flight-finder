---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "app-access",
      "effect": "changes"
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
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/cli/src/lib/access-cli.ts#registerAccessCommands"
    }
  ]
}
---

# Only Admin or the Instance operator changes the shared password

Admin changes it from Account security after verifying; the Instance operator resets it locally on the server.
