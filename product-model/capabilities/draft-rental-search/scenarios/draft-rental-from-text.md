---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Member describes the rental and asks for a draft",
      "kind": "actor",
      "actor": "member",
      "entities": [],
      "contexts": {
        "web": {
          "place": "web::travel::cars"
        }
      }
    },
    {
      "text": "The Product asks the configured language model for a draft and fills the form, leaving locations to choose from the catalog",
      "kind": "product",
      "actor": "member",
      "entities": [],
      "contexts": {
        "web": {
          "place": "web::travel::cars"
        }
      }
    }
  ]
}
---

# Draft a rental search

## Trigger

A Member describes a rental.

## Outcome

The form is prefilled for review; no search or tracker starts.
