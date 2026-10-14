---
{
  "availability": [
    {
      "place": "web::app-access"
    },
    {
      "place": "web::administration"
    }
  ],
  "domain": "app-access",
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "apps/web/src/app/access/AccessScreen.tsx"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "apps/web/src/app/access/security/SecurityScreen.tsx"
    }
  ]
}
---

# Save a passkey

Save a passkey with the device or a password manager so the app opens without the shared password next time. It is offered right after entering and from Account security.
