---
{
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/cli/src/lib/access-cli.ts#registerAccessCommands"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "apps/web/src/middleware.ts"
    }
  ]
}
---

# API device token

A scoped credential for a terminal client or agent that calls the instance's API without a browser session.

## Information kept

- **Name** — the optional device name
- **Profile** — the profile it was created for
- **Scope** — the API scope it grants
- **Token** — the secret shown once when it is created
