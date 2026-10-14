---
{
  "scope": "The self-hosted web app (access, flights, hotels, cars, notifications, settings, profiles) and the terminal access commands.",
  "method": "Static inspection of source, schema and documentation at 1e0ca1e; nothing was executed.",
  "covered": [
    {
      "description": "Shared access, profile selection, profiles and account settings",
      "paths": [
        "apps/web/src/app/access/",
        "apps/web/src/app/login/",
        "apps/web/src/app/api/access/",
        "apps/web/src/app/api/auth/",
        "apps/web/src/lib/sidedoor/",
        "apps/web/src/app/account/",
        "apps/web/src/app/api/account/",
        "apps/web/src/app/api/admin/users/",
        "apps/web/src/app/api/admin/multi-user/",
        "apps/web/src/app/admin/(dashboard)/users/",
        "apps/web/src/middleware.ts",
        "apps/web/src/lib/user-auth.ts",
        "apps/web/src/lib/multi-user.ts",
        "apps/web/src/lib/query-auth.ts",
        "apps/web/src/lib/account-migration.ts"
      ]
    },
    {
      "description": "Flight search, preview, tracking, price checks and charts",
      "paths": [
        "apps/web/src/app/page.tsx",
        "apps/web/src/app/q/",
        "apps/web/src/app/api/parse/route.ts",
        "apps/web/src/app/api/preview/",
        "apps/web/src/app/api/queries/",
        "apps/web/src/app/api/travel/",
        "apps/web/src/app/admin/(dashboard)/queries/",
        "apps/web/src/app/api/admin/queries/",
        "apps/web/src/lib/scraper/",
        "apps/web/src/lib/travel/",
        "apps/web/src/lib/cron.ts",
        "apps/web/src/components/"
      ]
    },
    {
      "description": "Hotel search, tracking and maps",
      "paths": [
        "apps/web/src/app/hotels/",
        "apps/web/src/app/api/hotels/",
        "apps/web/src/app/api/admin/hotel-map/",
        "apps/web/src/lib/hotels/"
      ]
    },
    {
      "description": "Car rental search, protection and tracking",
      "paths": [
        "apps/web/src/app/cars/",
        "apps/web/src/app/api/cars/",
        "apps/web/src/lib/cars/"
      ]
    },
    {
      "description": "Notification channels, price rules, recipients and delivery",
      "paths": [
        "apps/web/src/lib/notifications/",
        "apps/web/src/app/api/admin/notifications/",
        "apps/web/src/app/admin/(dashboard)/notifications/"
      ]
    },
    {
      "description": "Setup, instance settings and extraction configuration",
      "paths": [
        "apps/web/src/app/setup/",
        "apps/web/src/app/settings/",
        "apps/web/src/app/api/setup/",
        "apps/web/src/app/admin/(dashboard)/config/",
        "apps/web/src/app/api/admin/config/",
        "apps/web/src/app/api/vpn/"
      ]
    },
    {
      "description": "Persistence schema",
      "paths": [
        "apps/web/prisma/"
      ]
    },
    {
      "description": "Terminal access commands",
      "paths": [
        "packages/cli/src/lib/access-cli.ts"
      ]
    }
  ],
  "exclusions": [
    {
      "description": "Tests, fixtures and test harnesses",
      "paths": [
        "apps/web/src/test/",
        "scripts/",
        "packages/cli/src/__tests__/"
      ]
    },
    {
      "description": "CI, release and repository automation",
      "paths": [
        ".github/"
      ]
    },
    {
      "description": "Screenshots, demo media and design assets",
      "paths": [
        "assets/",
        "docs/"
      ]
    }
  ],
  "unmapped": [
    {
      "description": "Terminal client for flights, hotels and cars (search wizard, list, view, hotel and car commands, receipts)",
      "paths": [
        "packages/cli/src/app.tsx",
        "packages/cli/src/index.tsx",
        "packages/cli/src/screens/",
        "packages/cli/src/components/",
        "packages/cli/src/lib/car-cli.ts",
        "packages/cli/src/lib/hotel-cli.ts",
        "packages/cli/src/lib/parsing/"
      ]
    },
    {
      "description": "Background flight parsing jobs and their status API",
      "paths": [
        "apps/web/src/lib/parsing/",
        "apps/web/src/app/api/parse/[id]/"
      ]
    },
    {
      "description": "Hosted public website: explore, download, community hub, analytics and seed routes",
      "paths": [
        "apps/web/src/app/explore/",
        "apps/web/src/app/download/",
        "apps/web/src/app/api/community/",
        "apps/web/src/app/api/analytics/",
        "apps/web/src/app/admin/(dashboard)/analytics/",
        "apps/web/src/app/admin/(dashboard)/seed-routes/",
        "apps/web/src/app/api/admin/seed-routes/",
        "apps/web/src/lib/analytics/"
      ]
    },
    {
      "description": "Admin dashboard, airline insights, admin search, travel worker recovery and CLI model management",
      "paths": [
        "apps/web/src/app/admin/(dashboard)/page.tsx",
        "apps/web/src/app/admin/(dashboard)/insights/",
        "apps/web/src/app/admin/(dashboard)/search/",
        "apps/web/src/app/api/admin/insights/",
        "apps/web/src/app/api/admin/travel/",
        "apps/web/src/app/api/admin/cli-models/",
        "apps/web/src/app/api/setup/cli-models/",
        "apps/web/src/app/api/admin/local-models/",
        "apps/web/src/app/api/admin/providers/"
      ]
    },
    {
      "description": "Community data sync to the hub",
      "paths": [
        "apps/web/src/lib/community-sync.ts"
      ]
    },
    {
      "description": "Phone connection page and access invitations",
      "paths": [
        "apps/web/src/app/connect/",
        "apps/web/src/app/api/admin/access-invitation/"
      ]
    },
    {
      "description": "Desktop launcher, installer, updater and container entrypoint",
      "paths": [
        "apps/desktop/",
        "apps/web/public/",
        "bin/",
        "docker-entrypoint.sh"
      ]
    }
  ],
  "limitations": [
    {
      "description": "Shared-access screens and checks implemented inside the external shared-access package",
      "paths": [
        "apps/web/src/app/access/security/SecurityScreen.tsx",
        "apps/web/src/lib/sidedoor/access/access.ts"
      ]
    }
  ]
}
---

# Coverage
