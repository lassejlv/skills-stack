# skills-stack

The agent skills I use every day. Each folder in [`skills/`](skills) is a self-contained skill (a `SKILL.md` plus any references or scripts) that works with Claude Code, Codex, Grok and other agents that support the `SKILL.md` format.

## Install

Copy or symlink the skills into the folder your agent reads from:

```sh
# Claude Code (all projects)
ln -s "$PWD/skills/"* ~/.claude/skills/

# Codex / other agents that read .agents/skills
ln -s "$PWD/skills/"* ~/.agents/skills/
```

To use a single skill, link just that folder, e.g. `ln -s "$PWD/skills/tdd" ~/.claude/skills/tdd`.

## Skills

### Planning and thinking

| Skill | What it does |
| --- | --- |
| [grill-me](skills/grill-me) | A relentless interview to sharpen a plan or design. |
| [grill-with-docs](skills/grill-with-docs) | Same interview, writing ADRs and a glossary as it goes. |
| [grilling](skills/grilling) | Stress-test a plan, decision or idea. |
| [to-spec](skills/to-spec) | Turn the conversation into a spec on the issue tracker. |
| [to-tickets](skills/to-tickets) | Break a plan or spec into tracer-bullet tickets with blocking edges. |
| [to-questionnaire](skills/to-questionnaire) | Turn an open decision into a questionnaire for someone else. |
| [wayfinder](skills/wayfinder) | Plan work bigger than one session as a map of decision tickets. |
| [loop-me](skills/loop-me) | Grill me about specs for workflows I want to build. |
| [prototype](skills/prototype) | Build a throwaway prototype to answer a design question. |
| [research](skills/research) | Research a question against primary sources and save the findings. |
| [teach](skills/teach) | Teach a new skill or concept inside the workspace. |
| [wait-what](skills/wait-what) | Re-pitch the last message when it didn't land. |
| [chief-of-staff](skills/chief-of-staff) | Pursue a long-running goal by coordinating subagents. |
| [use-goal](skills/use-goal) | Durable goal sessions with memory, run through verified completion. |
| [project-roadmap](skills/project-roadmap) | Write a prioritized Markdown roadmap for the current project. |
| [project-board](skills/project-board) | A private `.board/BOARD.md` that keeps state between sessions. |
| [project-orientation-sweep](skills/project-orientation-sweep) | Map an unfamiliar repo before changing it. |

### Engineering workflow

| Skill | What it does |
| --- | --- |
| [implement](skills/implement) | Implement work from a spec or set of tickets. |
| [implement-spec](skills/implement-spec) | Implement the output of `/to-spec` and `/to-tickets`. |
| [tdd](skills/tdd) | Test-first development, red-green-refactor. |
| [diagnosing-bugs](skills/diagnosing-bugs) | Diagnosis loop for hard bugs and performance regressions. |
| [code-review](skills/code-review) | Review changes against repo standards and the originating spec. |
| [pr](skills/pr) | Write a PR body. |
| [triage](skills/triage) | Move issues and PRs through triage and write agent-ready briefs. |
| [retro](skills/retro) | Run a retrospective on a coding session. |
| [handoff](skills/handoff) | Compact the conversation into a handoff document. |
| [claude-handoff](skills/claude-handoff) | Hand the conversation to a fresh background agent. |
| [just-fucking-do-it](skills/just-fucking-do-it) | Finish an authorized task end to end instead of stopping at a plan. |
| [no-yak-shaving](skills/no-yak-shaving) | Keep changes proportionate to what was asked. |
| [wizard](skills/wizard) | Generate an interactive bash wizard for steps only a human can do. |
| [gitty](skills/gitty) | Generate repo-aware commit messages with the gitty CLI. |
| [setup-pre-commit](skills/setup-pre-commit) | Husky + lint-staged, type checking and tests on commit. |

### Architecture and code quality

| Skill | What it does |
| --- | --- |
| [codebase-design](skills/codebase-design) | Vocabulary for designing deep modules and placing seams. |
| [domain-modeling](skills/domain-modeling) | Build the domain model, glossary and ADRs. |
| [improve-codebase-architecture](skills/improve-codebase-architecture) | Find deepening opportunities and report them as HTML. |
| [untangle-codebase](skills/untangle-codebase) | Untangle a whole codebase so agents read less per change. |
| [clean-codebase](skills/clean-codebase) | Evidence-first repo-wide cleanup with eight subagents. |
| [setup-ts-deep-modules](skills/setup-ts-deep-modules) | Enforce deep-module boundaries with dependency-cruiser. |
| [migrate-to-shoehorn](skills/migrate-to-shoehorn) | Replace `as` assertions in tests with shoehorn. |
| [minimize-api-responses](skills/minimize-api-responses) | Trim API responses and enforce field-level authorization. |
| [scaffold-exercises](skills/scaffold-exercises) | Scaffold course exercises, problems and solutions. |

### Languages and frameworks

| Skill | What it does |
| --- | --- |
| [effect](skills/effect) | Production TypeScript with Effect v4. |
| [orpc](skills/orpc) | End-to-end typesafe APIs with oRPC v2. |
| [orpc-contract](skills/orpc-contract) | Contract-first oRPC APIs. |
| [the-cloudflare-stack](skills/the-cloudflare-stack) | TanStack Start, Better Auth, Drizzle, D1 and R2 on Cloudflare Workers. |
| [rust-best-practices](skills/rust-best-practices) | Write idiomatic, maintainable Rust. |
| [rust-port](skills/rust-port) | Port C, C++, Python, Go or TS to idiomatic Rust. |
| [rust-review](skills/rust-review) | Review Rust with a prioritized, rule-cited report. |
| [write-swift](skills/write-swift) | Modern Swift 6: concurrency, generics, testing, performance. |
| [build-gpui-apps](skills/build-gpui-apps) | Native Rust desktop apps with GPUI and GPUI Kit. |
| [paper-to-gpui](skills/paper-to-gpui) | Translate Paper.design frames into GPUI views. |
| [use-libtermy](skills/use-libtermy) | Embed Termy's terminal engine (Rust, C, Swift, web). |

### Design and UI

| Skill | What it does |
| --- | --- |
| [frontend-design](skills/frontend-design) | Distinctive, intentional visual design for new UI. |
| [design-taste-frontend](skills/design-taste-frontend) | Anti-slop rules for company and product websites. |
| [emil-design-eng](skills/emil-design-eng) | Emil Kowalski's approach to UI polish and details. |
| [apple-design](skills/apple-design) | Apple-style fluid motion, materials and typography for the web. |
| [scandinavian-design](skills/scandinavian-design) | A restrained black-and-white Scandinavian visual system. |
| [unslop](skills/unslop) | Turn AI-looking UI into a designed interface. |
| [no-vibe-code](skills/no-vibe-code) | Lint UI for generic generated design patterns. |
| [break-ui](skills/break-ui) | Break UI with worst-case data and fix what fails. |
| [mobile-native](skills/mobile-native) | Small CSS and meta fixes that make a web app feel native. |
| [learn-taste](skills/learn-taste) | Turn a session's design corrections into rules. |
| [pick-ui-library](skills/pick-ui-library) | Pick the right frontend library for a task. |
| [ask-sonner](skills/ask-sonner) | Guide to the Sonner toast library. |
| [use-design-system](skills/use-design-system) | Create or evolve a design system in Paper or Figma. |
| [create-ui-kit-from-website](skills/create-ui-kit-from-website) | Extract a website's visual system into a UI kit. |
| [use-svgl](skills/use-svgl) | Add official brand and tech logos from svgl.app. |
| [codex-image-generation](skills/codex-image-generation) | Generate images through the Codex CLI. |

### Animation

| Skill | What it does |
| --- | --- |
| [animate](skills/animate) | Build a web animation from scratch, decision by decision. |
| [animate-expo](skills/animate-expo) | Animations in React Native and Expo. |
| [animation-performance](skills/animation-performance) | Keep animations inside the frame budget. |
| [animation-vocabulary](skills/animation-vocabulary) | Name the motion effect you're describing. |
| [choreograph](skills/choreograph) | Coordinate several elements animating together. |
| [gestures](skills/gestures) | Drag, swipe and sheet interactions that track 1:1. |
| [find-animation-opportunities](skills/find-animation-opportunities) | Find places that should animate (read-only). |
| [improve-animations](skills/improve-animations) | Audit motion code and write implementation plans. |
| [remove-animations](skills/remove-animations) | Remove animations the interface doesn't need. |
| [review-animations](skills/review-animations) | Review motion code against a high craft bar. |

### Cloud and ops

| Skill | What it does |
| --- | --- |
| [use-aws](skills/use-aws) | Inspect and operate AWS accounts through the CLI. |
| [aws-account-cleanup](skills/aws-account-cleanup) | Dry-run-first teardown of AWS resources. |
| [gcp-account-cleanup](skills/gcp-account-cleanup) | Dry-run-first teardown of Google Cloud resources. |
| [sign-macos-for-github](skills/sign-macos-for-github) | Developer ID signing and notarization in GitHub Actions. |

### Writing

| Skill | What it does |
| --- | --- |
| [writing-fragments](skills/writing-fragments) | Mine raw fragments, no structure yet. |
| [writing-beats](skills/writing-beats) | Assemble raw material into a journey of beats. |
| [writing-shape](skills/writing-shape) | Shape raw material into an article. |
| [writing-for-agents](skills/writing-for-agents) | Write skills, AGENTS.md and CLAUDE.md. |
| [legal-policy-drafter](skills/legal-policy-drafter) | Draft terms and privacy policies from repo evidence. |

## Credits

Most of these come from other people's collections. Go star them:

- [mattpocock/skills](https://github.com/mattpocock/skills)
- [emilkowalski/skills](https://github.com/emilkowalski/skills)
- [lassejlv/skills](https://github.com/lassejlv/skills)
- [anthropics/skills](https://github.com/anthropics/skills)
- [Leonxlnx/taste-skill](https://github.com/Leonxlnx/taste-skill)
- [kitlangton/skills](https://github.com/kitlangton/skills)
- [middleapi/orpc](https://github.com/middleapi/orpc)
- [morganlinton/BeautifulRust](https://github.com/morganlinton/BeautifulRust)
- [ericzakariasson/scandinavian-design](https://github.com/ericzakariasson/scandinavian-design)
- [heydamir/unslop](https://github.com/heydamir/unslop)
- [caldoai/skills](https://github.com/caldoai/skills)
