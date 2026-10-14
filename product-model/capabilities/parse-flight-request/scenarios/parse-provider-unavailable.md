---
{
  "kind": "edge",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Member types a trip",
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
      "text": "The provider does not answer, so the Product shows \"Failed to parse query\"",
      "kind": "condition",
      "entities": [],
      "contexts": {
        "web": {
          "place": "web::travel::flights"
        }
      }
    }
  ]
}
---

# The language model is unavailable

## Trigger

The configured AI provider cannot be reached.

## Outcome

An error is shown; manual entry remains available.

## Edge cases

- Background parsing can be cancelled; an unconfirmed cancellation is reported as such.
