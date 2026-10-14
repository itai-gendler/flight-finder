---
{
  "kind": "validation",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "Admin chooses Add channel with a required field empty",
      "kind": "actor",
      "actor": "admin",
      "entities": [],
      "contexts": {
        "web": {
          "place": "web::administration::notifications"
        }
      }
    },
    {
      "text": "The Product refuses with the invalid setting",
      "kind": "condition",
      "entities": [],
      "contexts": {
        "web": {
          "place": "web::administration::notifications"
        }
      }
    }
  ]
}
---

# An invalid channel is refused

## Trigger

Required settings are missing.

## Outcome

Nothing is saved.
