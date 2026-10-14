---
{
  "kind": "edge",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Visitor opens the instance address",
      "kind": "actor",
      "actor": "visitor",
      "entities": [],
      "contexts": {
        "web": {
          "place": "web::app-access::open-flight-finder"
        }
      }
    },
    {
      "text": "No owner and shared password exist yet, so the Product shows that access must be set up in a terminal with flight-finder access setup",
      "kind": "condition",
      "actor": "visitor",
      "entities": [
        {
          "entity": "app-access",
          "effect": "reads",
          "facts": [
            "Owner set up"
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

# Entering before the first Admin exists

## Trigger

A Visitor opens a fresh instance whose access was not set up.

## Outcome

The screen asks for the local setup command; nothing can be entered yet.
