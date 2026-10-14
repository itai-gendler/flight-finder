---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Visitor chooses to open the app without the password next time and follows the device prompt",
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
      "text": "The Product saves the passkey",
      "kind": "product",
      "actor": "visitor",
      "entities": [
        {
          "entity": "passkey",
          "effect": "creates",
          "facts": [
            "Name",
            "Saved at"
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

# Save a passkey after entering

## Trigger

A Visitor has just entered the shared password.

## Outcome

A passkey is saved and opens the app on later visits.

## Edge cases

- Continue without a passkey skips saving.
- Passkeys need the instance's configured secure address and a compatible browser.
