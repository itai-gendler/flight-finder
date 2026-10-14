---
{
  "type": "cli",
  "actors": [
    "instance-operator"
  ],
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

# Terminal

The installed flight-finder command on the machine that runs the instance, used for local access administration.
