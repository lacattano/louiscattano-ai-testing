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

_No client engagements yet - first client is the priority (see [roadmap.md](roadmap.md)). The entry below is my own tool, not client work; it is here because it shows the method._

## clowder - own tool, agent dispatch (not a client engagement)

**Engagement:** Own product - no client, no fee. Listed as evidence of how I work.
**Dates:** 27-28 September 2026 (five commits, `git log --oneline`)
**Scope:** A Python CLI and a Pi skill that give a crew of coding agents one front door. It dispatches briefs, records state, and reports each answer with the question it answers attached. Each agent gets its own git worktree, so parallel work on one repo cannot collide.

### Outcome
- A written design of 19 numbered decisions, each with the reason and the rejected alternative (`DESIGN.md`). It names what was borrowed from [Firstmate](https://github.com/kunchenguid/firstmate) (ideas, no code) and what was left on purpose - their merge automation, because their tool merges and mine does not.
- Steps 1 to 4 built: the CLI, the front-door skill, the worktree and job machinery, and a generated HTML board. `/calm` is not built.
- Five gates - smoke, lint, format, type, tests - defined once in `scripts/check.py` and run as five separate checks in CI (`.github/workflows/ci.yml`), so the list a human runs and the list the robot runs cannot drift.
- The suite covers the CLI, state, git plumbing, the multiplexer adapter, the board and the skill (`tests/`).
- Python 3.14, standard library only, no dependencies (`pyproject.toml`).
- The tool never commits, pushes or merges; the merge is the human's step (`README.md`, decision 18 in `DESIGN.md`).
- Not finished: `/calm` is unbuilt, and `DESIGN.md` has an Open list - where reports should come from, how a clean merge is handled when both sides have moved, whether CI status belongs in a report, and whether a space per agent is right for a repo with large local test state.

### What the client said
No client - this is my own tool. The checkable substitutes are the design record and the CI workflow.

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
