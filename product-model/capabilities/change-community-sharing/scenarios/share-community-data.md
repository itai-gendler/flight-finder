---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "Admin turns on Community Data Sharing",
      "kind": "actor",
      "actor": "admin",
      "entities": [
        {
          "entity": "instance-settings",
          "effect": "reads",
          "facts": [
            "Community sharing"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::administration::instance-settings"
        }
      }
    },
    {
      "text": "The Product saves the choice and registers the instance for sharing",
      "kind": "product",
      "actor": "admin",
      "entities": [
        {
          "entity": "instance-settings",
          "effect": "changes",
          "facts": [
            "Community sharing"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::administration::instance-settings"
        }
      }
    }
  ]
}
---

# Share community data

## Trigger

Admin opts in.

## Outcome

Anonymized fares are shared; queries, preferences, keys and identity never are.

## Edge cases

- Accepting community registrations is off by default.
