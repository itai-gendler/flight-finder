---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "Admin sets the minimum drop and percentage and chooses Save thresholds",
      "kind": "actor",
      "actor": "admin",
      "entities": [
        {
          "entity": "instance-settings",
          "effect": "reads",
          "facts": [
            "Alert minimum drop",
            "Alert minimum percentage drop",
            "Public site URL"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::administration::notifications"
        }
      }
    },
    {
      "text": "The Product saves the thresholds",
      "kind": "product",
      "actor": "admin",
      "entities": [
        {
          "entity": "instance-settings",
          "effect": "changes",
          "facts": [
            "Alert minimum drop",
            "Alert minimum percentage drop",
            "Public site URL"
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

# Save thresholds

## Trigger

Admin wants fewer, larger alerts.

## Outcome

Later new-low alerts need the new drop.

## Edge cases

- Without a public site URL or APP_URL, alerts are sent without a link.
