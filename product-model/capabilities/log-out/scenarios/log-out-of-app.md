---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Member chooses Log out",
      "kind": "actor",
      "actor": "member",
      "entities": [],
      "contexts": {
        "web": {
          "place": "web::travel::flights"
        }
      }
    },
    {
      "text": "The Product signs this browser out",
      "kind": "product",
      "actor": "member",
      "entities": [
        {
          "entity": "browser-session",
          "effect": "removes"
        }
      ],
      "contexts": {
        "web": {
          "place": "web::travel::flights"
        }
      }
    }
  ]
}
---

# Log out

## Trigger

A Member chooses Log out or Switch user in the profile menu.

## Outcome

The browser must enter the shared password or a passkey again.
