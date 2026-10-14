---
{
  "entities": [
    {
      "entity": "hotel-tracker",
      "shows": [
        "Hotel name",
        "Stay",
        "Rooms and guests",
        "Latest price",
        "Match mode",
        "Target price",
        "Check interval",
        "Last error"
      ]
    },
    {
      "entity": "hotel-price-observation",
      "shows": [
        "Stay dates",
        "Total price",
        "Seller",
        "Room",
        "Match",
        "Eligible"
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
      "web": "/hotels/{id}"
    }
  ]
}
---

# Hotel tracker

One hotel tracker: stay details, latest price, history chart and table, alert settings, checks and, for Admin, its owner.
