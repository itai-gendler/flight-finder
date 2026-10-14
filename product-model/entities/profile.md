---
{
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "apps/web/prisma/schema.prisma"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "apps/web/src/app/api/account/settings/route.ts"
    }
  ]
}
---

# Profile

A named household profile chosen after entering the app. Trackers, preferences, avatar and theme are personal to a profile; profiles need no password of their own.

## Information kept

- **Username** — the unique name of the profile, 2 to 32 letters, numbers, dots, dashes or underscores
- **Display name** — the optional name shown instead of the username
- **Avatar** — one of the preset travel avatars, or initials
- **Theme** — the personal colour theme, falling back to the instance theme
- **Default currency** — the currency new searches use, falling back to the instance default
- **Default country** — the country new searches use, falling back to the instance default
- **Preferred airlines** — airlines new flight searches favour
- **Cabin class** — the cabin new flight searches use, falling back to economy
- **Flight source order** — the ordered price sources flight checks try, among those Admin allows
- **Car providers** — the ordered rental providers new car searches use, or both by default
- **Map style** — the preferred hotel map style
- **Map shown** — whether hotel results offer the map
