---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Member changes defaults and chooses Save",
      "kind": "actor",
      "actor": "member",
      "entities": [
        {
          "entity": "profile",
          "effect": "reads",
          "facts": [
            "Display name",
            "Default currency",
            "Preferred airlines",
            "Car providers"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::travel::account-settings"
        }
      }
    },
    {
      "text": "The Product saves the profile's settings",
      "kind": "product",
      "actor": "member",
      "entities": [
        {
          "entity": "profile",
          "effect": "changes",
          "facts": [
            "Display name",
            "Avatar",
            "Theme",
            "Default currency",
            "Default country",
            "Preferred airlines",
            "Cabin class",
            "Flight source order",
            "Car providers"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::travel::account-settings"
        }
      }
    }
  ]
}
---

# Save account settings

## Trigger

A Member opens Account & appearance.

## Outcome

New searches use the saved defaults; existing trackers are unchanged.

## Edge cases

- Only price sources Admin allows can be ordered.
- A provider order changed elsewhere meanwhile is refused with a request to reload.
