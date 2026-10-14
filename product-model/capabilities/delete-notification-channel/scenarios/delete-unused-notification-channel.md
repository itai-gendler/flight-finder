---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "Admin chooses Delete and confirms",
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
      "text": "The Product deletes the channel",
      "kind": "product",
      "actor": "admin",
      "entities": [
        {
          "entity": "notification-channel",
          "effect": "removes",
          "from": "Enabled"
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

# Delete a channel

## Trigger

Admin no longer uses a channel.

## Outcome

The channel is gone.

## Edge cases

- Trackers that chose the channel must remove it from their recipients before saving again.
