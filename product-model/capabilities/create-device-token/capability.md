---
{
  "availability": [
    {
      "place": "cli"
    }
  ],
  "domain": "app-access",
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

# Create an API device token

Create a scoped API token for a profile so a terminal client or agent can call the instance: flight-finder access device <principalId> [name].
