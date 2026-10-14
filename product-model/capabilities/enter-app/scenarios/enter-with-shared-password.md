---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Visitor enters the shared password and chooses Continue",
      "kind": "actor",
      "actor": "visitor",
      "entities": [
        {
          "entity": "app-access",
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
    },
    {
      "text": "The Visitor is taken to choose who is using the app",
      "kind": "condition",
      "actor": "visitor",
      "entities": [],
      "contexts": {
        "web": {
          "place": "web::app-access::open-flight-finder"
        }
      }
    }
  ]
}
---

# Enter with the shared password

## Trigger

A Visitor opens the instance address.

## Outcome

The browser is admitted and lands on the profile picker.

## Edge cases

- A wrong password is refused with "The credentials could not be verified."
- Repeated attempts are refused for a while with "Too many attempts. Try again later."
