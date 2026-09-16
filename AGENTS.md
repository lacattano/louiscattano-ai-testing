# AGENTS.md — Louis Cattano AI-Assisted Test Automation (business track)

> This is the **business / marketing repo** for Louis Cattano's contractor
> services (AI-assisted test automation). It is NOT the product repo.
> The product (now branded **TanCat**, repo `tancat-ai/tancat`, Apache-2.0)
> lives at `C:\Users\l_a_c\code\AI-Playwright-Test-Generator` (local folder
> name is unchanged).

---

## 1. What This Project Is

A set of plain-markdown business documents: positioning, offer, pricing,
case-study template, landing-page draft, and a kanban-lite roadmap. No code,
no build, no tests. Every file is marketing copy that must stay **honest and
verifiable** — the whole pitch rests on trust ("reviewed by a human QA
engineer", "AI speed without the risk").

---

## 2. Golden Rules

### Product stats — never guess, always verify
- ✅ Marketing claims about the product (test counts, accuracy gates, features)
  MUST be checked against the product repo **before** writing or editing them.
  Source of truth: `CHANGELOG.md` [Unreleased] → latest gate lines
  ("N pytest passed", "eval static X%").
- ❌ NEVER round up, extrapolate, or reuse an old number because it's "close enough".
  A stale metric repeated across files is the #1 failure mode of this repo
  (it shipped with 2,260/95.2% while the product was already past 2,300/97.9%).
- ✅ When the product's numbers move, update **all** claim sites in one commit:
  `README.md`, `offer.md`, `landing.md` (and `pricing.md` if it cites anything).

### No invented outcomes
- ✅ Case studies / testimonials only from **real** engagements; results must be
  facts the owner confirms (see `case-studies.md` — it already requires written
  permission before publishing names).
- ❌ NEVER fabricate client quotes, outcomes, or delivery dates.
- ❌ NEVER mark roadmap items done without the owner's confirmation or
  repo-visible evidence (e.g. the "publish repo" box was left unchecked while
  the commit existed — check evidence, then ask).

### Positioning integrity
- ✅ The "honest bit" is deliberate: agents write implementation, the owner
  reviews/tests/ships. Preserve this framing — do not soften it into
  suggesting the owner hand-writes code, and do not oversell AI as autonomous.
- ❌ Don't add prices, services, or engagement terms that aren't already in the
  docs — pricing changes need the owner.
- ❌ All content is **proprietary — no open-source license applies.** Don't add
  license files or OSS-friendly wording.

---

## 3. File Map

| File | Role | Edit rules |
|------|------|------------|
| `README.md` | Positioning + index of the repo | Keep table of contents in sync |
| `offer.md` | Fixed-scope "AI Test Automation Setup" (2 weeks, £2k–£4k) | Scope/price changes need owner |
| `pricing.md` | Day rate, setup, teaching rates | Price changes need owner |
| `case-studies.md` | Template for client outcomes | Fill only from real engagements |
| `landing.md` | Draft GitHub Pages landing copy | Draft may diverge from README; flag it |
| `roadmap.md` | Kanban-lite: Now / Next / Later / Ideas | Status only on owner confirmation |
| `upskilling.md` | Playwright/pytest upskilling plan + progress log | Truthful claims only — the CV's Playwright line depends on this |

---

## 4. Working Here

- ✅ Small, focused edits; one logical change per commit; review
  `git diff` before committing.
- ✅ Markdown conventions: title links to repo files, consistent £ / rate
  formatting, UK English spelling.
- ✅ Keep cross-file claims consistent — same numbers, same offer terms,
  same tone. If you spot drift, fix all copies or flag it.
- ✅ When editing after product development: check `CHANGELOG.md` in the
  product repo for new features worth surfacing (self-healing locators,
  cited generation, credential redaction) and ask the owner whether to
  feature them.

---

## 5. When to Ask First

- Any pricing / offer / engagement-term change
- Any claim about the owner's real-world status (contracts, clients,
  networking, LinkedIn, agencies) — only they know
- Publishing `landing.md` (needs the owner to actually deploy GitHub Pages)
- Anything that moves `roadmap.md` status

---

## 6. Known Sync Points (verify before use)

As of 2026-09-11, the product repo's latest recorded gate: **3,123 pytest
passed**, eval static 97.9%, ruff + mypy clean (`CHANGELOG.md`, WebP-evidence
entry). Verify against `CHANGELOG.md` before writing it anywhere — this line
goes stale fast.

**Scope caveat — do not drop this when copying the 97.9%:** that figure is the
*static eval on frozen scraped captures*, not live regeneration against a real
site. The product's own `docs/plans/NEXT_SESSIONS_IMPROVEMENTS.md` (2026-09-15)
records live regeneration at ~50% on a plain static page, ~10 false greens in
one 48-test run, and self-healing not yet effective (B-068). Never present
97.9% as end-to-end trustworthiness, and don't market self-healing until that
item lands. Whenever a claim is written here, ask: what exactly does the number
measure, and on what set?

*Last updated: 2026-09-16*