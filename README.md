# Norawat Vera

I'm the CIO at Maverix Group (Feb 2021 to now). We distribute 10+ premium Italian motorcycle brands in Thailand, for example Italjet, Brembo and SC-Project.
Most of my recent work is replacing paid SaaS with our own apps. I write the spec, build with AI coding tools, review and test the code, ship it, and train the staff.

This repo is case studies only. No source code.

## Projects

| Project | What it replaced | Stack | Result |
|---|---|---|---|
| [DHumanice HR and payroll](projects/dhumanice-hr.md) | ByteHR | Next.js, Expo React Native, Supabase, react-pdf | Whole company (7 departments) clocks in, requests leave and gets paid through it. iOS and Android apps in the stores |
| [Tequila task management](projects/tequila.md) | ClickUp (rollout in progress) | Next.js, Supabase, pg_cron, Web Push | Boards, automation rules, recurring tasks, email digest, browser push. About 3,000 automated tests |
| [Maverix Club loyalty CRM](projects/maverix-club-crm.md) | EGG Digital's CRM | Next.js, LINE LIFF, Supabase, SMS OTP | About 1,900 members imported. Cancelled a 360,000 THB/yr contract |
| [Brembo product registration](projects/brembo-registration.md) | Nothing (new) | Next.js, LINE LIFF, Supabase, satori | Stock team scans serials, customers register in LINE and get a warranty certificate |
| [Italjet digital service book](projects/italjet-service-book.md) | Paper service books | Next.js, LINE LIFF, Supabase | Dealers log services, owners see their bike history in LINE. In user testing |
| [QuickBooks connector for Claude](projects/quickbooks-mcp.md) | Manual QuickBooks exports | Node.js, MCP SDK, OAuth 2.0, Supabase | 32 tools the accounting team used from Claude. Since retired |
| [Italjet chat funnel on Respond.io](projects/respondio-italjet.md) | Unstructured chat replies | Respond.io workflows, n8n, REST API | 6 live workflows for test-ride booking plus a weekly KPI email |
| [WooCommerce event booking plugin](projects/woocommerce-booking-plugin.md) | Hard-coded booking form | PHP, WooCommerce, PHPUnit | Configurable Thai/English booking form with guest checkout |
| [Websites and automation](projects/websites-and-automation.md) | Manual work across tools | Cloudways, Cloudflare, n8n, Make.com, inFlow | 15 websites, 11 shops tied to inventory, the glue between systems |

## Side projects

| Project | What it is | Stack | Result |
|---|---|---|---|
| [Multi-Claude](projects/multi-claude.md) | Desktop app for running several Claude Code sessions, with account hot-swap even mid-session (plus Codex and Antigravity in terminal view), with Phumipat Jiranarongwat (main author). I do the macOS version | Electron, TypeScript, React | Used by his coworkers. About 4,100 tests |
| [Thai to English novel translation](projects/novel-translation.md) | AI translation workflow for a Thai novelist | Claude, ChatGPT, Claude in Chrome | 11 books on Amazon Kindle |
| [3D-printed pill cutter](projects/pill-cutter.md) | Two-blade cutter that cuts a tablet into thirds, rebuilt from an open design with a Python script | Python, trimesh, Bambu Studio, PETG | Three printable versions to pick the most even split |

## Skills

- TypeScript, Next.js, React, React Native (Expo), Node.js, PHP
- Postgres and Supabase: row-level security, SQL functions, pg_cron, migrations
- LINE platform (LIFF, Login, Messaging API), Respond.io, WooCommerce, QuickBooks Online API
- n8n and Make.com, REST APIs, webhooks, OAuth
- DigitalOcean App Platform, Docker, Cloudways, Cloudflare
- Testing: Vitest, Playwright, PHPUnit, written UAT scripts
- Business systems rollout: Monday.com company-wide, then ClickUp, now moving to our own Tequila

## How I work

- Claude Code every day. ChatGPT and Gemini too.
- Spec and UI mockups first, then build. Staff pick the design before any UI code.
- Automated tests on every change, plus code review by a second model and OWASP checks.
- Postgres row-level security on every table that holds staff or customer data.
- Step-by-step UAT scripts for the people who will use the app, then training.

## Savings

So far DHumanice and the CRM replaced ByteHR (30,000 THB/yr) and EGG (360,000 THB/yr). All 5 apps run for about 38,000 THB/yr on DigitalOcean and Supabase. Net, about 350,000 THB/yr saved.

The code belongs to the company and is private. I'm happy to demo the live apps in an interview.

Contact: norawat.w@gmail.com
