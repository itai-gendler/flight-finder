---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "device-token",
      "effect": "creates"
    }
  ],
  "permits": [
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
      "target": "packages/cli/src/lib/access-cli.ts#registerAccessCommands"
    }
  ]
}
---

# Only the Instance operator creates API device tokens

Device tokens are created locally on the server with flight-finder access device.
