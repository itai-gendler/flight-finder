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
      "target": "apps/web/public/flight-finder-cli"
    }
  ]
}
---

# Set up access

Create the first Admin profile and the shared password in a terminal on the server: flight-finder access setup. The installer runs it; unattended installs keep sign-in closed until it is run.
