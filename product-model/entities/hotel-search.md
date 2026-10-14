---
{
  "domain": "hotels",
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "apps/web/src/lib/hotels/store.ts#createHotelSearch"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "apps/web/src/lib/hotels/types.ts"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "apps/web/src/lib/hotels/domain.ts#validateHotelSearch"
    }
  ]
}
---

# Hotel search

A search of Google Hotels and Booking.com for a stay. Searches run in the background; a hotel tracker's scheduled checks are hotel searches too.

## Information kept

- **Destination** — the place to stay
- **Stay dates** — check-in and check-out, fixed, nearby dates or a window with minimum and maximum nights
- **Rooms and guests** — one to four rooms, each with adults and children's ages
- **Currency** — the price currency
- **Sources** — Google Hotels, Booking.com or both
- **Filters** — budget, refundable, breakfast, hotel class, guest rating, amenities and excluded sellers
- **Offers** — the qualifying offers found, with totals including taxes and fees
- **Provider errors** — each source and stay that failed, with its message
- **Progress** — stays checked of the total
- **Imported link** — the hotel link the search was imported from, if any
- **Owner** — the profile it belongs to

## States

### Queued

Waiting to run.

### Running

Sources are being checked.

### Completed

Finished, possibly with provider errors.

### Failed

Could not complete.

### Cancelled

Stopped by its owner, or because its tracker was paused or changed.
