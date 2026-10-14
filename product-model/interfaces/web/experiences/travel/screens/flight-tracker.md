---
{
  "entities": [
    {
      "entity": "flight-tracker",
      "shows": [
        "Route",
        "Travel dates",
        "Label",
        "Last check",
        "Tracking ends",
        "Comparison countries",
        "Check interval",
        "Notification recipients"
      ]
    },
    {
      "entity": "fare-observation",
      "shows": [
        "Price",
        "Airline",
        "Travel date",
        "Observed at",
        "Booking link",
        "Country"
      ]
    },
    {
      "entity": "tracker-edit",
      "shows": [
        "Edited at",
        "Summary"
      ]
    },
    {
      "entity": "price-rule",
      "shows": [
        "Scope",
        "Target price",
        "Absolute drop",
        "Percentage drop"
      ]
    },
    {
      "entity": "notification-channel",
      "shows": [
        "Label",
        "Type"
      ]
    },
    {
      "entity": "instance-settings",
      "shows": [
        "Allowed price sources"
      ]
    }
  ],
  "entryPoints": [
    {
      "web": "/q/{id}"
    }
  ]
}
---

# Flight price chart

One tracker or tracker group: price evolution, best price, price history, calendar, filters, sources, check interval, label, alert recipients and price rules.
