---
{
  "availability": [
    {
      "place": "web::app-access"
    }
  ],
  "domain": "app-access",
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "apps/web/src/app/access/page.tsx"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "apps/web/src/app/access/AccessScreen.tsx"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "apps/web/src/lib/sidedoor/access/access.ts#accessHandler"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "apps/web/src/middleware.ts"
    }
  ]
}
---

# Enter the app

Open the instance with the shared password or a saved passkey. Entering admits the browser; the person then chooses a profile.
