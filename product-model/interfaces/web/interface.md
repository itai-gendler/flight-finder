---
{
  "type": "web",
  "actors": [
    "visitor",
    "member",
    "admin"
  ],
  "entryPoints": [
    {
      "web": "/"
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "apps/web/src/middleware.ts"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "apps/web/src/app/page.tsx"
    }
  ]
}
---

# Web

The self-hosted web app, reached from a browser or installed on a phone as an app. Everything except entering the app needs an admitted browser.
