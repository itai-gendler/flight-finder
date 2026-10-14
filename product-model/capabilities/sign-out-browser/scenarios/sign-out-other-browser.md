---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "Admin chooses Sign out beside a signed-in browser",
      "kind": "actor",
      "actor": "admin",
      "entities": [
        {
          "entity": "browser-session",
          "effect": "reads",
          "facts": [
            "Browser",
            "Signed in at"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::administration::account-security"
        }
      }
    },
    {
      "text": "The Product signs that browser out",
      "kind": "product",
      "actor": "admin",
      "entities": [
        {
          "entity": "browser-session",
          "effect": "removes"
        }
      ],
      "contexts": {
        "web": {
          "place": "web::administration::account-security"
        }
      }
    }
  ]
}
---

# Sign out another browser

## Trigger

Admin sees a browser that should no longer have access.

## Outcome

That browser must enter again.
