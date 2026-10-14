---
{
  "id": "flight-finder",
  "summary": "Self-hosted flight, hotel and car rental price tracking with natural-language search, price history and alerts.",
  "category": "travel",
  "tags": [
    "travel",
    "price-tracking",
    "self-hosted",
    "flights",
    "hotels",
    "car-rental"
  ],
  "authors": [
    {
      "name": "Andres Romero",
      "url": "https://github.com/affromero"
    }
  ],
  "license": "MIT",
  "languages": [
    "en",
    "de",
    "es",
    "fr",
    "pt"
  ],
  "limitations": [
    "Flight, hotel and car trackers are independent; they are never combined into a package, shared itinerary or combined budget.",
    "Bookings are completed with the airline, hotel seller or rental provider; Flight Finder never reserves, books or buys anything.",
    "Prices are compared in one currency without currency conversion.",
    "Unverified prices, fees, occupancy or requested policies are never guessed; they stay unverified and cannot alert.",
    "One shared password opens the app; profiles separate trackers and preferences and need no second password."
  ],
  "references": [
    {
      "kind": "doc",
      "role": "intent",
      "target": "README.md"
    },
    {
      "kind": "doc",
      "role": "intent",
      "target": "API.md"
    },
    {
      "kind": "doc",
      "role": "context",
      "target": "AGENTS.md"
    }
  ]
}
---

# Flight Finder

Flight Finder tracks flight, hotel and car rental prices on your own server. You describe a trip in plain
language (or fill a form), review the fares, hotels or rentals it finds, and choose what to track. Each
tracker is checked on a schedule; its price history is kept on your instance and price alerts go to the
notification channels you configure. A household shares one instance: everyone enters with the same
password or a saved passkey and chooses a profile, and with multi-user mode on each profile has its own
trackers and preferences while Admin manages the instance.

## Intent

"The price trail airlines don't show you." Airlines change prices constantly and the companies with the
history keep it to themselves; Flight Finder keeps that history for you, privately, on infrastructure you
control, using your own AI provider (or none, for hotels and cars). Searches stay private, the scrape
frequency is yours, and many small self-hosted instances make quiet requests instead of one central service.
