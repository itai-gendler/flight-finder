---
{
  "kind": "validation",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "Admin enters a style URL with credentials or a query string and saves",
      "kind": "actor",
      "actor": "admin",
      "entities": [],
      "contexts": {
        "web": {
          "place": "web::administration::instance-settings"
        }
      }
    },
    {
      "text": "The Product refuses with \"Map URLs must use HTTPS without credentials, query strings or fragments\"",
      "kind": "condition",
      "entities": [],
      "contexts": {
        "web": {
          "place": "web::administration::instance-settings"
        }
      }
    }
  ]
}
---

# Unsupported map addresses are refused

## Trigger

The style URL is not public HTTPS.

## Outcome

Nothing is saved.

## Edge cases

- Same-origin styles must live under /maps/; at most eight resource origins.
