---
{
  "kind": "alternative",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Visitor chooses Sign in with a passkey and confirms with the device",
      "kind": "actor",
      "actor": "visitor",
      "entities": [
        {
          "entity": "passkey",
          "effect": "reads",
          "facts": []
        }
      ],
      "contexts": {
        "web": {
          "place": "web::app-access::open-flight-finder"
        }
      }
    },
    {
      "text": "The Product admits this browser for the household",
      "kind": "product",
      "actor": "visitor",
      "entities": [
        {
          "entity": "browser-session",
          "effect": "creates",
          "facts": [
            "Browser",
            "Signed in at"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::app-access::open-flight-finder"
        }
      }
    }
  ]
}
---

# Enter with a saved passkey

## Trigger

A Visitor whose browser saved a passkey opens the instance.

## Outcome

The browser is admitted without typing the password.
