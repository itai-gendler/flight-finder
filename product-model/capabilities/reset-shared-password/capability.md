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
    }
  ]
}
---

# Reset the shared password

Replace a lost shared password locally on the server: flight-finder access reset. Reset revokes existing sessions and passkeys.
