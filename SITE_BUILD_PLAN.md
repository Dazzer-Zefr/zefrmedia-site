# ZEFR MEDIA — SITE BUILD PLAN
*This file lives in the repo root. It is the single source of truth for build state.*
*Every session: read this first. Every session: update it and push before ending.*

---

## LOCKED STRUCTURE (from Zefr_Site_Structure_FINAL.xlsx — do not invent sections)

Nav order: **PLATFORM · GAMING · BETTING · GROWTH · SERVICES · COMPANY · NORM.GAME** + "Start a Project" pill

| Pillar | Pages |
|---|---|
| Platform | PAM · Technology & Infrastructure · Payments · Compliance & Risk |
| Gaming | Casino · Live Casino · Sweepstakes & Social · Content & Aggregation |
| Betting | Sportsbook ✅ · Prediction Markets |
| Growth | Acquisition · Retention · Support |
| Services | Consulting · Web & Design |
| Company | About |
| NORM.GAME | Splash (last in nav, never hero) |

Sportsbook locked sections (reference): Odds · Trading · Risk · Live/In-Play · Sports Data Feeds.
Each new page's sections come from the spreadsheet — **read it, never guess**.

---

## PAGE STATUS

| Page | Research | Copy | Build | Verified | Pushed |
|---|---|---|---|---|---|
| Homepage | ✅ | ✅ | ✅ | ✅ Playwright 1280+390 (lean rebuild re-verified Session A) | ⬜ push (Session A batch) |
| Sportsbook | ✅ | ✅ | ✅ | ✅ re-verified Session A after token/font fixes | ⬜ push (Session A batch) |
| Prediction Markets | ✅ Kalshi/Polymarket/ICE/Matchbook/Shift (Session A) | ✅ | ✅ | ✅ Playwright 1280+390, screenshots reviewed | ⬜ push (Session A batch) |
| PAM | ⬜ | ⬜ | ⬜ | ⬜ | ⬜ |
| Technology & Infrastructure | ⬜ | ⬜ | ⬜ | ⬜ | ⬜ |
| Payments | ⬜ | ⬜ | ⬜ | ⬜ | ⬜ |
| Compliance & Risk | ⬜ | ⬜ | ⬜ | ⬜ | ⬜ |
| Casino | ⬜ | ⬜ | ⬜ | ⬜ | ⬜ |
| Live Casino | ⬜ | ⬜ | ⬜ | ⬜ | ⬜ |
| Sweepstakes & Social | ⬜ | ⬜ | ⬜ | ⬜ | ⬜ |
| Content & Aggregation | ⬜ | ⬜ | ⬜ | ⬜ | ⬜ |
| Acquisition | ⬜ | ⬜ | ⬜ | ⬜ | ⬜ |
| Retention | ⬜ | ⬜ | ⬜ | ⬜ | ⬜ |
| Support | ⬜ | ⬜ | ⬜ | ⬜ | ⬜ |
| Consulting | ⬜ | ⬜ | ⬜ | ⬜ | ⬜ |
| Web & Design | ⬜ | ⬜ | ⬜ | ⬜ | ⬜ |
| About | ⬜ | ⬜ | ⬜ | ⬜ | ⬜ |

Research already banked (reusable): Traffic pillar (35 companies), Stake + bet365 operator patterns
("owning the stack beats renting"), GiG/Affilka/L&W/Lion design analysis, Hub88/GR8 buyer criteria.
Thin pillars needing fresh research: Game Provider, Certification, Platform/Prediction, Payment, Compliance & Fraud.

---

## BUILD ORDER (2 pages per session, fully done)

1. **Session A — Prediction Markets + template extraction.** Prediction Markets is Sportsbook's
   sibling: proves the template transfers. Extract `_TEMPLATE.html` from sportsbook.html with
   marked slots. Also: performance pass — extract base64 assets from index.html (2.2MB HTML),
   convert bg PNGs → WebP.
2. **Session B — PAM + Payments** (Platform anchor pages; buyers' first technical questions)
3. **Session C — Technology & Infrastructure + Compliance & Risk** (completes Platform)
4. **Session D — Casino + Content & Aggregation**
5. **Session E — Live Casino + Sweepstakes & Social** (completes Gaming)
6. **Session F — Acquisition + Retention**
7. **Session G — Support + Consulting**
8. **Session H — Web & Design + About** (About = the 1995→now timeline; delete or keep orphaned
   old discipline pages — decide here)

---

## DEFINITION OF DONE (no page ships without all six)

1. **Research pass** — competitors for that vertical fetched and read *this session*, not recalled
2. **Copy draft** — plain capability+outcome headers (GiG SportX model: "Your prices. Your margin.");
   concrete texture: named integrations, metrics, certifications — never adjectives (Affilka standard)
3. **Build on template** — sections from spreadsheet only; design-system classes, zero inline-style layout
4. **Playwright verify** — 1280px and 390px; check: fonts loaded, borders render, animations run,
   no JS errors, no horizontal overflow, section order matches spreadsheet
5. **Screenshots reviewed** — actually looked at, not just "tests passed"
6. **Status updated + pushed** — this file's table updated, committed, pushed same session

---

## DESIGN LAWS (violations = redo)

- Design system is locked — brand tokens only: `--ink #08060F · --mag #FF2E9E · --vio #8A2BE2 ·
  --cyan #3CE0E0 · --gold #E8B84B · --white #F6F4FB · --muted #A99FC4 · --line rgba(255,255,255,.11)`
- Fonts: Anton (display) · Archivo (body) · **JetBrains Mono (console/data UI — must be in the import link)**
- Each section does a **different job** — never enumerate the same list twice
- Numbered markers (01/02/03) only for genuine sequences (About timeline qualifies; capability lists never)
- Depth = composited scenes (bg image/video → glow layer → foreground cutout), never flat bordered panels
- **One signature element per page** — spend the boldness in one place, keep the rest disciplined
- No mirrored text-left/visual-right column reflex; no stacked twin 50/50 grids
- Hero CTA: single pill, "Start Your [Pillar] Project"
- `iGaming` always via `.ig` helper (lowercase i)

---

## SIGNATURE GRAPHIC PER PAGE (built in HTML/CSS/SVG, brand tokens, no stock)

| Page | Signature element | Hero treatment |
|---|---|---|
| Prediction Markets | Live probability bars shifting on simulated market events | bg-network.jpg composite |
| PAM | Player account dashboard mock — KYC state, wallet, live session row | CDN video 1 |
| Technology & Infrastructure | Uptime/latency ticker + animated architecture diagram | bg-network.jpg composite |
| Payments | Payment routing flow animation, approval-rate counter climbing | CDN video 2 |
| Compliance & Risk | Jurisdiction/licence badge wall + scrolling risk-flag feed | dark composite + gold accents |
| Casino | Game-tile carousel with RTP/volatility hover data | bg-towers.jpg composite |
| Live Casino | Table stream UI mock with seat map + live bet overlay | CDN video 3 |
| Sweepstakes & Social | Dual-currency wallet toggle (GC/SC) animating balances | violet composite |
| Content & Aggregation | Single-API diagram: many providers → one integration line | bg-network.jpg composite |
| Acquisition | Funnel visualization with CAC/LTV counters | CDN video 4 |
| Retention | Cohort retention curve drawing itself + CRM journey nodes | cyan composite |
| Support | SLA response ticker + chat-thread mock | dark composite |
| Consulting | Engagement timeline: audit → plan → build → operate | minimal, type-led |
| Web & Design | Design-system specimen (the site's own tokens as the exhibit) | self-referential |
| About | 1995→2026 operator timeline (numbered — a true sequence) | bg-towers.jpg composite |

Asset pipeline: cleared images = bg-towers.jpg, bg-network.jpg (from investor PDF, approved public).
CDN videos: `vid.cdn-website.com/27af0057/videos/` (4 interior backgrounds). Everything else is
code-built. **Convert PNGs → WebP before production. Extract base64 blobs from index.html.**

---

## HARD CONSTRAINTS (never violate)

- betED/WINBOB name and logo: **never** on public pages; rebuild UI clean in Zefr brand, no blurring
- "Top-**five** North American sportsbook" — never top-ten
- NORM.GAME: transaction COUNT only, never dollar value; no financials, raise terms, or mechanics on public pages
- NORM.GAME appears last in nav; splash page, never a hero element
- Nothing saved to shared Notion/Drive (partner surprise)
- Build sessions run in Claude Code on Darren's machine — it has the repo and GitHub auth and pushes directly; commit + push before ending every session

---

## SESSION PROTOCOL — CLAUDE CODE (all sessions from Session B onward)

Sessions run in Claude Code, in the local clone of `Dazzer-Zefr/zefrmedia-site`.
No file shuttling between chat and repo — the repo is the memory.

**Start of session:**
1. `git pull` — never build on a stale tree
2. Read this file (SITE_BUILD_PLAN.md) top to bottom
3. Read the per-page section list from Zefr_Site_Structure_FINAL.xlsx (keep a copy at repo root as `_structure.xlsx` so it's always available) — sections come from the sheet, never invented
4. Fresh competitor research for the pages being built this session — fetched now, not recalled

**Build:**
5. New pages descend from `_TEMPLATE.html` — replace SLOT blocks only, never touch CONSTANT blocks
6. Definition of Done applies in full (research → copy → build → Playwright 1280+390 → screenshots actually reviewed → status updated)
7. Playwright runs locally; screenshots saved to `_verify/` (gitignored)

**End of session:**
8. Update the PAGE STATUS table and OPEN ITEMS in this file
9. Append a dated entry to the session log
10. `git add -A && git commit && git push` — a session isn't over until the push lands and the Cloudflare deploy is spot-checked live

## OPEN ITEMS

- [ ] Push Session A files via Claude Code (one-time: HTML + media downloaded from the chat outputs)
- [ ] Confirm live after Cloudflare deploy: index (should be ~40KB, JetBrains Mono present), sportsbook, prediction-markets
- [ ] Decide how prediction-markets.html is reached in the nav (BETTING currently links only to sportsbook.html — dropdown? links between the two Betting pages?)
- [ ] If a newer verified sportsbook.html exists on Darren's machine, upload it to the next chat — the repo version + Session A fixes is the current best known copy
- [ ] Compress img/bg-towers.jpg + img/bg-network.jpg → WebP (repo originals still JPEG; low priority, they're already reasonably sized)
- [ ] Decide fate of orphaned pages: strategy-consulting / design-marketing / technology-ai / igaming.html (Session H)
- [ ] Homepage "What We Do" cards still carry old discipline names (Strategy Consulting / Design & Marketing / Technology & AI / iGaming) linking to new pillar pages — verified last session as-is; revisit if wanted

## SESSION A LOG (July 2026)

- **File mix-up resolved:** the file uploaded as "sportsbook.html" was actually the verified lean-target homepage (title, six-section spine, in-play console). The real sportsbook was already in the repo, missing the JetBrains Mono import and brand-token `--line`.
- **Performance pass done on index.html:** 2.2MB → 39.7KB. Extracted 3 base64 JPEGs → WebP (home-hero/home-cta/home-poster) and 1 embedded base64 MP4 (~1.2MB) → img/home-hero.mp4. Added missing NORM.GAME nav link (locked-structure violation).
- **Sportsbook fixed in place:** `--line` → rgba(255,255,255,.11); JetBrains Mono added to import + applied to console/numeric UI; off-brand #7af0c0 green → var(--cyan).
- **_TEMPLATE.html extracted** from fixed sportsbook with marked SLOT/CONSTANT comments (title/meta, subnav, hero+signature+stats, sections, ctaband, page JS).
- **prediction-markets.html built** — fresh research: ~$24B/mo market, sports-led (~80% on the lead exchange), ICE's $2B Polymarket stake, DraftKings–Railbird, Robinhood–MIAXdx, FanDuel–CME, Matchbook Predictions + Shift Markets as embed routes, CFTC-vs-gaming-rails split, Gibraltar first EU licence. Sections: Overview · The Product · Routes In · Regulation · Zefr's Role. Signature element: live probability board (YES/NO cent pricing, animated bars, volume ticker). Hero on bg-network, bigband on bg-towers.
- **All three pages Playwright-verified** at 1280 + 390: no JS errors, no horizontal overflow, Anton/Archivo/JetBrains Mono render-measured (not just fonts.check), homepage clock + sportsbook clock/odds + prediction board/volume all tick. Screenshots reviewed.
