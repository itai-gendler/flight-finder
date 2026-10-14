---
{
  "availability": [
    {
      "place": "web::administration"
    }
  ],
  "domain": "settings",
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "apps/web/src/app/settings/page.tsx"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "apps/web/src/app/api/vpn/status/route.ts"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "apps/web/src/components/vpn/VpnPreferences.tsx"
    }
  ]
}
---

# Change VPN price comparison

Save the ExpressVPN activation code so prices can be compared from other countries; the readiness of the VPN is checked after saving.
