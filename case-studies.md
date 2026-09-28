# Case Studies & Testimonials

Template for recording client work. Fill in after each engagement — these
become the social proof for the landing page and future proposals.

## Template

```markdown
## [Client name / anonymised] — [industry]

**Engagement:** [AI Test Automation Setup / Contract / Training]
**Dates:** [start] – [end]
**Scope:** [what we built — journeys, stack, CI]

### Outcome
[What changed: e.g. "16 critical journeys covered by Playwright tests
running in CI; regression suite runs in <x> min on every push"]

### What the client said
> [quote]

### What I'd do differently next time
[one honest line]

### Links
[product used / repo / CI badge]
```

## Completed

_No client engagements yet - first client is the priority (see [roadmap.md](roadmap.md))._

## Own work - clowder, agent dispatch

_My own tool, not a client engagement - evidence of the method the [setup service](offer.md) sells, kept separate from client outcomes._

**Engagement:** Own product - no client, no fee.
**Dates:** 27-28 September 2026 (`git log --oneline`)
**Scope:** A Python CLI and a Pi skill that give a crew of coding agents one front door. It dispatches briefs, records state, and reports each answer with the question it answers attached. Each agent can have its own git worktree, so parallel work on one repo does not have to share a checkout.

Running one agent is easy. Running four is where it breaks, and not because of the agents: you become the integration layer, carrying who is on what, which question is still unanswered, and which pane you spoke to last. Answers arrive with nothing to say which question they answer. That is bookkeeping, and bookkeeping should not live in your head.

### Outcome
- A written design of 19 numbered decisions, each with the reason and the rejected alternative (`DESIGN.md`). It names what was borrowed from [Firstmate](https://github.com/kunchenguid/firstmate) (ideas, no code) and what was left on purpose - their merge automation, because their tool merges and mine does not.
- Steps 1 to 4 built: the CLI, the front-door skill, the worktree and job machinery, and a generated HTML board. `/calm` is not built.
- Five gates - smoke, lint, format, type, tests - defined once in `scripts/check.py` and run as five separate checks in CI (`.github/workflows/ci.yml`), so the list a human runs and the list the robot runs cannot drift.
- The suite covers the CLI, state, git plumbing, the multiplexer adapter, the board and the skill (`tests/`).
- Python 3.14, standard library only, no dependencies (`pyproject.toml`).
- The tool never commits, pushes or merges; the merge is the human's step (`README.md`, decision 18 in `DESIGN.md`).
- Not finished: `/calm` is unbuilt, and `DESIGN.md` has an Open list - where reports should come from, how a clean merge is handled when both sides have moved, whether CI status belongs in a report, and whether a space per agent is right for a repo with large local test state.

### In use

In one session I dispatched ten tasks through it, with three agents working at once, each in its own worktree. Two of those changes reached `main` after review, each with all five checks green:

- [pull request 1](https://github.com/lacattano/clowder/pull/1) - merge `034a38b`
- [pull request 2](https://github.com/lacattano/clowder/pull/2) - merge `4aef13f`

The CI runs are linked from those pages. One worker also refused a fix whose premise turned out to be wrong - the page the fix depended on was not recorded in the plan it was sent to - and reported why instead. That is the behaviour the design was built for: an answer that says what it checked, not only what it did.

### Why it exists

[Firstmate](https://github.com/kunchenguid/firstmate) already states the one-liaison idea, and this design started from it - ideas borrowed, no code. It was still written for three reasons. Firstmate targets macOS and Linux with tmux, zellij or cmux; this is Windows with herdr. It supports eight harnesses; this supports one, Pi. And it merges to main and opens pull requests, while here the merge stays the human's step. That is a difference in scope, not a claim to be better.

### What I'd do differently next time
Write the gate list before the first test. It arrived late (commit `8097417`, after steps 1 to 4), and until then "run the tests" lived only in prose.

### Links
- [clowder on GitHub](https://github.com/lacattano/clowder) (MIT)
- Design and decisions: `DESIGN.md`
- Gates: `scripts/check.py` - CI: `.github/workflows/ci.yml`

---

## Notes

- Anonymise or get written permission before publishing names
- The productized setup service doubles as product research — note any
  generator features the engagement surfaced (missing locator patterns,
  UI friction, new export needs) and feed them to the product backlog
