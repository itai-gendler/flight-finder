---
{
  "availability": [
    {
      "place": "cli"
    }
  ],
  "domain": "settings",
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/cli/src/lib/access-cli.ts#registerAccessCommands"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "apps/web/src/lib/sidedoor/access/network/configuration.ts"
    }
  ]
}
---

# Configure the login address

Set the exact public address people sign in from, such as a tunnel or custom hostname: flight-finder access origin <url>. It also repairs a login blocked by an unconfigured address and supplies alert links.
