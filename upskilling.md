# Upskilling Plan — Playwright & pytest

**Goal:** be able to write and defend a Playwright + pytest test from scratch —
enough to clear a technical screen for a test automation contract.

**Why:** the CV lists Playwright (via the TanCat project) and states Playwright
as the current upskilling focus. This plan is what makes that claim true, and
produces a public artifact to point at instead of asking a client to take it
on trust.

---

## Method

- Build a small **public practice repo**, start to finish. Commit daily — the
  repo becomes the interview artifact.
- Use AI to **explain**, not to write your first draft. Type the first version
  yourself; that is where the learning happens.
- **Scope discipline:** pytest + Playwright + CI only. No TypeScript, no
  mobile, no visual testing, no framework-building from scratch.
- Expect roughly half the time to go on debugging. Debugging *is* the skill.

---

## Week 1 — foundations and first own test

| Day | Focus | Done when |
|-----|-------|-----------|
| 1 | Install Python/uv + Playwright + pytest. Write **one** test by hand against saucedemo login (no AI drafting) | A passing test you wrote |
| 2 | Locators: `get_by_role`, `get_by_label`, `get_by_text`, `get_by_test_id`, CSS. Rewrite day 1 role-based | You can fix a deliberately broken locator |
| 3 | pytest fixtures, `conftest.py`, parametrisation; refactor into a small Page Object | 3 tests + POM + fixture |
| 4 | Full journey: login → browse → cart → checkout → assert confirmation | 5–8 tests covering a journey |
| 5 | Debugging + traces (`--tracing on`, trace viewer); push to GitHub + GitHub Actions workflow | Green CI badge on a public repo |

## Week 2 — consolidate and prove

- **6–7:** data-driven tests, negative cases (wrong password), API testing with
  `requests`/pytest — builds on existing API-testing background, so this should
  be quick.
- **8:** take a **TanCat-generated** suite, read it line by line, explain every
  line, repair a locator by hand. Doubles as dogfooding and product feedback.
- **9:** mock interview — "walk me through your framework", "why role-based
  locators", "how do you handle flakiness", "fix this failing test live".
  Record yourself.
- **10:** write a README explaining the framework and how you'd onboard a new
  tester into it.

---

## Definition of done

The bar that makes the CV claim honest:

- [ ] Write a passing 3-test suite from scratch in under an hour, without copying
- [ ] Explain every line of it
- [ ] Fix a broken locator live
- [ ] Have a public repo with green CI to point at
- [ ] Answer: what's a fixture / why role-based locators / how do you debug flakiness

Once these are true, move Playwright/Python out of **Currently Upskilling** and
into **Core Competencies** on the CV, and add the practice repo link.

---

## Skills gate: Git

Being able to call Git a core competency means doing the everyday workflow
unaided and being able to explain it — not knowing Git internals. It is a day or
two of work, and most of it happens in Week 1 of this plan for free (the
practice repo is committed daily, pushed to GitHub, CI on every push).

Add ~2 hours on the [Git Handbook](https://docs.github.com/en/get-started/using-git/about-git)
and [learngitbranching.js.org](https://learngitbranching.js.org).

- [ ] Explain in your own words what a commit, a branch and a remote are
- [ ] Do the daily loop unaided: `status` → `diff` → `add` → `commit` → `push` → `pull`
- [ ] Create a branch, work on it, merge it back
- [ ] Resolve a simple merge conflict
- [ ] Open a pull request on GitHub and understand the review/merge flow
- [ ] Undo: discard a change, undo the last commit, restore a file
- [ ] Explain what `.gitignore` is and why it matters

Once ticked, add Git to **Core Competencies** on the CV.

---

## Two tracks — run in parallel

- **Track A (now):** apply to roles that match what can already be defended —
  Guidewire test automation, insurance QA, Geb/Spock, contract QA. Do **not**
  gate all applications on finishing this plan.
- **Track B (2 weeks):** the plan above.

The 18-month employment gap is covered by the TanCat project: it reads as
"building a product and upskilling", not idling, provided the CV shows dates.

---

## Progress log

| Date | Day | What I did | Notes / what was hard |
|------|-----|------------|-----------------------|
| | | | |
| | | | |
| | | | |

---

## Practice repo

- Repo: _(to be created)_
- CI badge: _(to be added)_
