---
{
  "singleton": true,
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "apps/web/prisma/schema.prisma"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "apps/web/src/app/api/admin/config/route.ts"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "apps/web/src/lib/multi-user.ts#isMultiUserEnabled"
    }
  ]
}
---

# Instance settings

The instance-wide configuration Admin manages in Settings, Extraction Config and Notifications.

## Information kept

- **AI provider** — the language model provider used to read requests and extract prices
- **Model** — the selected model and, for subscription CLIs, its reasoning effort
- **Provider credentials** — saved, encrypted keys or endpoints for the provider; never shown again
- **Check interval** — the default hours between scheduled price checks
- **Default currency** — the instance currency, or detected automatically
- **Default country** — the instance country, or detected automatically
- **Default search method** — whether the flight search opens with natural language or manual entry
- **Theme** — the instance colour theme
- **Allowed price sources** — the flight price sources members may use; Skyscanner and Kayak are off by default
- **Scraping** — On while background price checks run; Off pauses all of them
- **Extraction limits** — the extraction timeout, maximum flights per date, maximum flights tracked per route and maximum preview combinations
- **Rate limits** — per-provider request caps and preview concurrency limits
- **Alert minimum drop** — the smallest absolute drop, in the tracker's currency, that makes a new-low flight alert; 5 by default
- **Alert minimum percentage drop** — an extra percentage gate on new-low flight alerts; 0 disables it
- **Public site URL** — the exact address people use to reach the instance; it also supplies links in alerts
- **VPN provider** — ExpressVPN or Mullvad, used to compare prices from other countries
- **VPN activation code** — the saved, encrypted activation code
- **Default VPN countries** — countries compared when a tracker names none
- **Community sharing** — whether anonymized fares are shared with the community dataset
- **Community registrations** — whether this instance accepts other instances as a community hub
- **Multi-user mode** — Off for a single Admin profile; On for household profiles with personal trackers
- **Setup complete** — whether first-run setup has finished
- **Hotel map provider** — OpenFreeMap or a custom MapLibre style with its resource origins and attribution, and whether maps are available
