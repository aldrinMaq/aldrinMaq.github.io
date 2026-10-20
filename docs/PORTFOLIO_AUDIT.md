# Portfolio audit — October 2026

**Target role:** remote fullstack developer, Java/Spring Boot + Vue.js/TypeScript.
**Reader:** an engineering manager or technical recruiter giving the page about 30 seconds.

## Baseline vs after (Lighthouse 12.8, local, simulated mobile)

| Category | Before | After |
| --- | --- | --- |
| Performance (mobile) | 48 | 89–95 (varies run to run) |
| Performance (desktop) | — | 98 |
| Accessibility | 100 | 100 (no axe-core failures) |
| Best practices | 96 | 100 |
| SEO | 100 | 100 |
| Mobile LCP | 6.4 s | ~1.1 s |
| Console warnings | Tailwind CDN "not for production" | none |

Main cause before: the Tailwind CDN script and the Font Awesome JS kit blocked rendering for about 5.5 s.

## Ranked findings (what a 30-second reader missed)

1. **The page loaded slowly on phones (6.4 s LCP) and showed a console warning.** For a frontend hire, the site is a work sample. *Fixed:* prebuilt Tailwind CSS (`npm run build:css`), inline SVG icons, non-blocking fonts, deferred rendering for lower sections.
2. **The DinkSpot link was broken.** `dink-spot.vercel.app/map` returns 404 when opened directly, because the Vercel project has no SPA rewrite. *Fixed here:* the link now points to the root URL. *Still open:* add a `vercel.json` rewrite in the dink-spot repo.
3. **The stack was not visible above the fold.** The hero said "Fullstack Web Developer" but never named Java/Spring Boot or Vue. *Fixed:* a stack line, an "open to remote · UTC+8" badge, and resume numbers as stat tiles.
4. **Projects had no visual proof.** Only Growgreen had images. *Fixed:* live screenshots for every project, plus a stack chip row on each card. GoFindPro is now the featured card, with a problem statement taken from its concept doc.
5. **DinkSpot copy was stale.** It mentioned "verification status", but that model was removed in the repo (`Remove subscription/verified model`). *Fixed:* it now describes what exists: indoor/outdoor filters, Suggest Edit, and an installable PWA.
6. **The PoC was buried.** The Node.js data-sync PoC is the clearest sign of architectural judgment. *Fixed:* experience bullets are grouped as Backend / Architecture / Frontend / Quality / Team (wording unchanged from the resume).
7. **Education layout.** The incomplete IT degree had the same visual weight as the CS degree. *Fixed:* that card is now muted.
8. **No link preview, favicon, or structured data.** *Fixed:* OG/Twitter tags, a 1200×630 `assets/og-image.png`, an SVG favicon, a canonical URL, and Person JSON-LD.
9. **Thesis photos were 0.4–1.2 MB JPGs.** *Fixed:* WebP copies in `assets/img/` (13–40 KB) with `srcset`.

## Gap matrix (sample of remote Java + Vue postings)

Sources: Randstad Deutschland senior Java/Vue (arc.dev), Interactivated senior Java/Vue (join.com), HeyApril Spring Boot + Vue + TS (Bossjob, PH, 3–5 yrs), Link Group mid fullstack (justjoin.it), Jobgether full-stack listing. This is a small sample, and several of the postings have expired.

| Requirement seen in postings | On site? | With evidence? | Notes |
| --- | --- | --- | --- |
| Java + Spring Boot | Yes | Yes: mykuan.app APIs, Growgreen | Core match |
| Vue.js incl. state mgmt | Yes | Yes: GoFindPro (Pinia), 15+ components | Core match |
| TypeScript | Yes | Yes: GoFindPro, WeatherCheck, DinkSpot | |
| REST API design | Yes | Yes: 30+ APIs | No API example or diagram shown |
| Relational DB (PostgreSQL) | Skills only | **No** | Gap: name the DB used at mykuan.app if true, or add a project that uses it |
| Automated testing | Yes | Yes: Selenium, 30% | Gap: no unit/integration testing (JUnit, Vitest) shown |
| CI/CD, Docker | Skills only | **No** | Gap: one sentence on where you used them, if true |
| Kubernetes / cloud | No | No | Common in senior postings; not on resume, so don't add it |
| Messaging (Kafka, RabbitMQ) | No | No | Senior-only in this sample |
| Architecture decisions | Yes | Partly: Node.js PoC | Could become a short write-up of what the PoC tested and decided |
| Code review / mentoring | No | No | Add only if true |
| Years of experience | 3+ | Yes | Fits mid-level (3–5 yrs); senior postings ask 5–7+ |

**Most valuable next content (needs facts from you):** one or two sentences each on the database, Docker, and CI/CD you actually used at mykuan.app, and a short note on what the data-sync PoC compared and what was decided.

## 5-second test script (run with 3–5 people)

1. Send the link. Say: "Look at this page for 5 seconds, then close it."
2. Ask:
   - What role is this person looking for?
   - What's their main tech stack?
   - Name one project you remember.
   - Would you click through to learn more? Why or why not?
3. Pass: at least 3 of 5 say "fullstack / remote" **and** "Java/Spring + Vue" **and** name a project.
4. Then give them 30 seconds and ask: "Which link would you click first?" (first-click test).

## Still open

- **Analytics:** create a GoatCounter (free) or Plausible account. Then I can add the script and click events for projects, resume, and email.
- **DinkSpot SPA rewrite:** add `vercel.json` with a rewrite to `/index.html` in the dink-spot repo so deep links like `/map` work.
- **OG preview check:** after you push, paste the URL into LinkedIn Post Inspector and opengraph.xyz.
- **LinkedIn link:** add it if you have a profile.
- **GitHub:** turn on "Private contributions" in profile settings; consider one small public sample repo.
- **Original JPGs** (`IMG_20250501_*.jpg`) are no longer referenced by the page. Keep them out of the commit or move them elsewhere.
