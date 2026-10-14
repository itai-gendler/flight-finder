---
{
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "apps/web/src/lib/sidedoor/access/service.ts"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "apps/web/src/app/api/auth/login/route.ts"
    }
  ]
}
---

# Signed-in browser

A browser that has entered the app and keeps access until it signs out or its session lapses.

## Information kept

- **Browser** — the browser and device
- **Signed in at** — when it entered
- **Selected profile** — the profile currently chosen in this browser, if any
