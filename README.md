# Texas Parse Cloud — Parse.com Revived ☁️🛢️

Facebook built Parse. Facebook abandoned it. 600,000 apps left homeless. This is the Texas revival.

**Live repo facts (verified Oct 21, 2026):** 487 tracked files | 5,744 commits | Apache 2.0 | Built in Abilene, TX
**Base:** [parse-community/parse-server](https://github.com/parse-community/parse-server) **v9.10.6-alpha.5** — see Disclosure below.

[![License: Apache 2.0](https://img.shields.io/badge/License-Apache_2.0-blue.svg)](LICENSE)
[![Texas Edition](https://img.shields.io/badge/Texas-Edition-red.svg)](https://github.com/RJF-72/parse-server-texas-edition)

---

## 💰 HOSTED — $99/mo UNLIMITED

Don't want to self-host? I host it for you — Texas support, from Abilene.

👉 **Order by email today:** rjflanary1@gmail.com — onboarding is personal, I set you up myself.
👉 **Payhip checkout:** https://payhip.com/b/Kila5 · Direct checkout: https://payhip.com/order?link=Kila5

> **Status (Oct 21, 2026):** LIVE and verified — product page and subscription checkout both load with the $99/mo price. Prefer email? rjflanary1@gmail.com works too.

✅ Unlimited apps, requests, users
✅ MongoDB + Redis + S3 included — no extra bills
✅ Free migration from Heroku / Back4App / Firebase — I do it TODAY
✅ Email: rjflanary1@gmail.com — Abilene, TX

Why $99? Back4App's unlimited-requests Dedicated plan is $400/mo. Firebase bills by usage, with lock-in and no self-host option. Texas Parse Cloud is $99 flat.

---

## 🛢️ What Is This?

This is [parse-community/parse-server](https://github.com/parse-community/parse-server) (40k+ stars, Apache 2.0, battle-tested) — imported as the **Texas Edition**:

- **Original upstream:** https://github.com/parse-community/parse-server
- **This edition:** Texas branding + $99/mo hosted offer + one-click Docker deploy (this repo)
- **License:** Apache 2.0 — free to use, modify, and sell. See [LICENSE](LICENSE) and [NOTICE](NOTICE).
- **Full upstream documentation:** preserved in [UPSTREAM_README.md](UPSTREAM_README.md) and at https://parseplatform.org

### ⚠️ Disclosure — read before you buy or deploy

This Texas Edition is based on upstream parse-server **v9.10.6-alpha.5**, which is an **alpha (pre-release)** build, not a stable 8.x release. It passed our install/build/boot checks (see Health Check below), but alpha software can change or break between releases. For a production workload that cannot tolerate that, ask about pinning to the latest stable upstream release instead — email rjflanary1@gmail.com.

---

## ⚡ Quick Start — Self-Host FREE

**Requirements:** Node.js 20.19+ / 22.13+ / 24.11+ (see `engines` in `package.json`) and MongoDB 7 or 8 running locally (or use Docker below).

```bash
git clone https://github.com/RJF-72/parse-server-texas-edition.git
cd parse-server-texas-edition
npm install

PARSE_SERVER_APPLICATION_ID=TEXAS \
PARSE_SERVER_MASTER_KEY=change-this-to-a-long-random-secret \
PARSE_SERVER_DATABASE_URI=mongodb://localhost:27017/dev \
npx parse-server

# API: http://localhost:1337/parse
# Health check: http://localhost:1337/parse/health  →  {"status":"ok"}
```

> **Fix note:** the environment variables are the `PARSE_SERVER_*` names above. Short names like `APP_ID` / `MASTER_KEY` / `DATABASE_URI` are **not** read by this server and will be silently ignored. Copy `.env.example` for the supported settings, or run `npx parse-server --help`.

### Or Docker (recommended — includes MongoDB + Redis):

```bash
git clone https://github.com/RJF-72/parse-server-texas-edition.git
cd parse-server-texas-edition
cp .env.example .env        # set your own MASTER_KEY in .env first!
docker compose up -d
# API: http://localhost:1337/parse
```

Optional Parse Dashboard (local use only):

```bash
docker compose --profile dashboard up -d
# Dashboard: http://localhost:4040  (login from your .env — change it before any public deploy)
```

---

## 📦 Texas Deploy Files

| File | What it is |
|---|---|
| `Dockerfile` | Production-ready multi-stage build (upstream, Node 20.19 Alpine) |
| `docker-compose.yml` | **New in Texas Edition** — Parse Server + MongoDB 7 + Redis 7, one command |
| `.env.example` | **New in Texas Edition** — every required setting, with the correct `PARSE_SERVER_*` names |
| `package.json` | parse-server 9.10.6-alpha.5 |
| `LICENSE` / `NOTICE` | Apache 2.0, upstream attribution preserved |
| `UPSTREAM_README.md` | Full original parse-server README / configuration reference |

---

## 🆚 vs Others

|  | Texas Parse Cloud | Back4App | Firebase |
|---|---|---|---|
| Price | **$99/mo unlimited** | $80/mo for 5M req; $400/mo unlimited | usage-based, lock-in, no self-host |
| Open source | ✅ Apache 2.0 | ❌ | ❌ |
| Self-host free | ✅ | ❌ | ❌ |

---

## 🏗️ Repo Health Check — Oct 21, 2026 (verified, not marketing)

✅ Public repo, `main` branch, **487 tracked files, 5,744 commits**, Apache 2.0
✅ `npm ci` — PASS (1,571 packages, clean install)
✅ `npm run build` — PASS (Babel, 197 files compiled to `lib/`)
✅ CLI boot — PASS (config parses with `PARSE_SERVER_*` env; server starts and connects to MongoDB)
✅ `src/`, `spec/`, `public/`, `bin/`, `Dockerfile` all present
✅ `docker-compose.yml` + `.env.example` added in Texas Edition (compose not run on the build box — no Docker there; file is spec-valid YAML)
⚠️ Base is an **alpha** upstream release (9.10.6-alpha.5) — see Disclosure above
✅ Payhip — FIXED Oct 21, 2026: the Kila5 product existed as an unpublished, invisible DRAFT membership (that is why the links redirected/404'd). It is now Published + Visible: product page and $99/mo subscription checkout verified live
⚠️ 5 upstream Dependabot PRs open (#1–#5): four are major-version bumps (release tooling / bcrypt / Babel) and are **not** blind-merged; reviewed individually

Repo is OK — ready to sell, with the disclosures above on the label.

---

## 💳 Payhip $99/mo — Links

- Sales page: https://payhip.com/b/Kila5
- Checkout: https://payhip.com/order?link=Kila5
- Support: rjflanary1@gmail.com

*Parse is a trademark of its respective owner; this project is an independent hosted edition of the open-source Parse Server (Apache 2.0), imported from the upstream project; not affiliated with Meta/Facebook or the Parse Platform project.*
