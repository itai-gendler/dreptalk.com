---
{
  "scope": "The DRepTalk app worker, its governance sync worker and the drep.link worker, at their core governance and forum workflows.",
  "method": "Static reading of source, configuration and the shipped help guides; no code was run.",
  "covered": [
    {
      "description": "Forum threads, posts, reactions, flags, versions and search.",
      "paths": [
        "src/lib/forum/",
        "src/lib/cip100/",
        "src/lib/search/",
        "config/categories.ts",
        "src/lib/markdown.ts"
      ]
    },
    {
      "description": "Sign-in, sessions, device pairing, co-proposer mandates and moderator roles.",
      "paths": [
        "src/lib/auth/",
        "src/pages/api/auth/",
        "config/moderators.ts"
      ]
    },
    {
      "description": "Governance action mirror, tallies, votes, voting and submission.",
      "paths": [
        "src/lib/governance/",
        "src/lib/koios/",
        "src/lib/wallet/",
        "src/lib/cardano/",
        "src/pages/api/gov-action/",
        "src/pages/api/vote/",
        "src/pages/api/drep/",
        "config/proposers.ts"
      ]
    },
    {
      "description": "DRep profiles, matching and drep.link.",
      "paths": [
        "src/lib/dreps/",
        "src/lib/drepLink/",
        "src/lib/match/",
        "workers/drep-link/",
        "config/drepLinkReserved.ts"
      ]
    },
    {
      "description": "Delegation following and the delegator pages.",
      "paths": [
        "src/lib/delegation/",
        "src/pages/api/delegation/"
      ]
    },
    {
      "description": "Notifications, push and the Telegram bot.",
      "paths": [
        "src/lib/notifications/",
        "src/lib/push/",
        "src/pages/api/notifications/",
        "src/pages/api/telegram/"
      ]
    },
    {
      "description": "CIP-179 survey mirror and answering.",
      "paths": [
        "src/lib/surveys/"
      ]
    },
    {
      "description": "Governance Review editions and their announcement.",
      "paths": [
        "src/lib/review/",
        "src/content/review/"
      ]
    },
    {
      "description": "Analytics and treasury tracking.",
      "paths": [
        "src/lib/analytics/",
        "src/lib/treasury/",
        "config/ncl-periods.ts"
      ]
    },
    {
      "description": "Scheduled sync worker and its phases.",
      "paths": [
        "workers/gov-sync/",
        "src/lib/sync/",
        "src/lib/freshness.ts"
      ]
    },
    {
      "description": "Stored data access.",
      "paths": [
        "src/lib/db/"
      ]
    },
    {
      "description": "Pages, components and layouts of the website.",
      "paths": [
        "src/pages/",
        "src/components/",
        "src/layouts/"
      ]
    }
  ],
  "exclusions": [
    {
      "description": "Help guides, glossary and legal pages, which are shipped content.",
      "paths": [
        "src/content/guides/",
        "src/content/glossary/",
        "src/lib/help/",
        "src/lib/glossary/",
        "src/lib/legal.ts"
      ]
    },
    {
      "description": "Social preview images, brand assets and static files.",
      "paths": [
        "src/pages/og/",
        "src/lib/og/",
        "src/lib/brand/",
        "assets/",
        "public/"
      ]
    },
    {
      "description": "Build, deployment, CI and developer tooling.",
      "paths": [
        "scripts/",
        ".github/",
        "patches/",
        "docs/",
        "astro.config.mjs",
        "wrangler.toml"
      ]
    },
    {
      "description": "Database schema migrations.",
      "paths": [
        "migrations/"
      ]
    },
    {
      "description": "HTTP plumbing, caching, rate limiting and the worker entry.",
      "paths": [
        "src/lib/http/",
        "src/middleware.ts",
        "src/worker.ts",
        "src/lib/rate.ts",
        "src/lib/rateLimiterDO.ts"
      ]
    },
    {
      "description": "Machine-readable feeds and exports: sitemaps, llms.txt, CSV exports and structured data.",
      "paths": [
        "src/pages/sitemap.xml.ts",
        "src/pages/sitemap-cip100.xml.ts",
        "src/pages/llms.txt.ts",
        "src/lib/llms/",
        "src/lib/jsonld/",
        "src/pages/treasury/[periodId].csv.ts",
        "src/pages/vote/record.csv.ts"
      ]
    },
    {
      "description": "The operator's sync status page.",
      "paths": [
        "src/pages/debug/"
      ]
    }
  ],
  "unmapped": [
    {
      "description": "Badge awards and badge pages.",
      "paths": [
        "src/lib/badges/",
        "config/badges.ts",
        "src/lib/db/badgeAwards.ts",
        "src/pages/badges.astro",
        "src/pages/dreps/[drepId]/badges.astro"
      ]
    },
    {
      "description": "Voting-power origins page for DReps.",
      "paths": [
        "src/pages/voting-power-origins.astro",
        "src/pages/api/drep/voting-power-origins.ts"
      ]
    },
    {
      "description": "Per-vote statement pages and short vote links.",
      "paths": [
        "src/pages/dreps/[drepId]/vote/",
        "src/pages/spos/",
        "src/pages/s/"
      ]
    },
    {
      "description": "DRep statistics digest notifications.",
      "paths": [
        "src/lib/db/drepStatsDigest.ts",
        "src/lib/notifications/drepStats.ts"
      ]
    },
    {
      "description": "Anti-spam guard for the moderated Telegram group.",
      "paths": [
        "src/lib/notifications/telegramGroupGuard.ts"
      ]
    },
    {
      "description": "DRep movers page.",
      "paths": [
        "src/pages/dreps/movers.astro"
      ]
    }
  ],
  "limitations": []
}
---

# Coverage
