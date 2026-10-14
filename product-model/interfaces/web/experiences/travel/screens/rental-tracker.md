---
{
  "entities": [
    {
      "entity": "rental-tracker",
      "shows": [
        "Label",
        "Rental criteria",
        "Tracking mode",
        "Latest price",
        "Revision",
        "Target price"
      ]
    },
    {
      "entity": "rental-price-observation",
      "shows": [
        "Rental total",
        "Payment timing",
        "Deposit",
        "Excess",
        "Eligible"
      ]
    },
    {
      "entity": "price-alert",
      "shows": [
        "Delivered channels",
        "Last error"
      ]
    },
    {
      "entity": "profile",
      "shows": [
        "Display name"
      ]
    }
  ],
  "entryPoints": [
    {
      "web": "/cars/{id}"
    }
  ]
}
---

# Rental tracker

One rental tracker: settings and revision, price evidence, check history, provider errors and notification delivery.
