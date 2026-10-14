---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "Admin chooses to disable multi user mode on Users and confirms",
      "kind": "actor",
      "actor": "admin",
      "entities": [],
      "contexts": {
        "web": {
          "place": "web::administration::users"
        }
      }
    },
    {
      "text": "The Product turns multi-user mode off",
      "kind": "product",
      "actor": "admin",
      "entities": [
        {
          "entity": "instance-settings",
          "effect": "changes",
          "facts": [
            "Multi-user mode"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::administration::users"
        }
      }
    }
  ]
}
---

# Disable multi user mode

## Trigger

Admin no longer wants separate profiles.

## Outcome

The instance is single-profile again.
