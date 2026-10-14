---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "Admin chooses Send test",
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
      "text": "The Product sends a test message through the channel and shows the result",
      "kind": "product",
      "actor": "admin",
      "entities": [
        {
          "entity": "notification-channel",
          "effect": "reads",
          "facts": [
            "Type",
            "Settings"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::administration::notifications"
        }
      }
    }
  ]
}
---

# Send a test

## Trigger

Admin wants to confirm a channel works.

## Outcome

The row shows Test sent or the provider error.

## Edge cases

- Tests are rate limited.
