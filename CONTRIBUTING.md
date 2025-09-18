# Contributing to <PROJECT_NAME>

Thank you for your interest in contributing! This repository is a reusable template intended to accelerate creation of new business website projects. It intentionally includes placeholders that SHOULD be updated when you instantiate a real project. Look for angle‑bracket placeholders like `<PROJECT_NAME>` and follow the Checklist for Template Consumers section to customize them.

> Replace this introductory paragraph with a concise project description once the template is cloned for a real project.

---

## Quick Start (TL;DR)
1. Fork / create a new repo from this template.
2. Run initial setup steps in `docs/setup-guide.md`.
3. Create a feature branch from the default development branch (see Branching Model).
4. Make changes, add/update tests (if/when added), run linters/formatters.
5. Use a Conventional Commit message (see Commit Convention).
6. Open a Pull Request (PR) and fill out the PR template (add one if missing).
7. Ensure all checks pass and request review from a code owner.
8. After approval & checks pass, squash merge (recommended) or follow release procedure (see Releases) if applicable.

---

## Table of Contents
- Project Roles & Ownership
- Code of Conduct
- Governance / Decision Making
- Branching Model
- Issue Workflow
- Commit Convention
- Pull Request Guidelines
- Code Style & Tooling
- Testing Guidelines
- Documentation Standards
- Dependency Management
- Security & Responsible Disclosure
- Releases & Versioning
- Changelog Management
- Infrastructure / Deployment (Template Notes)
- Template Consumer Customization Checklist
- FAQ

---

## Project Roles & Ownership
| Role | Placeholder | Responsibilities |
|------|-------------|------------------|
| Product Owner | `<PRODUCT_OWNER_NAME>` | Prioritize backlog, accept features |
| Technical Lead | `<TECH_LEAD_NAME>` | Architecture, code quality, reviews |
| Maintainers | `<MAINTAINERS>` | Approvals, triage issues |
| Security Contact | `<SECURITY_CONTACT>` | Vulnerability response |

Update these entries when instantiating a real project. If no formal roles exist, collapse this section.

---

## Code of Conduct
This project follows the guidelines in `CODE_OF_CONDUCT.md`. By participating you agree to uphold them. Escalation path: contact `<PROJECT_CONTACT_EMAIL>` or the security contact for sensitive concerns.

---

## Governance / Decision Making
Lightweight governance model:
- Small fixes: Any maintainer can merge after one approving review.
- Features: Require at least 1 maintainer review + confirmation from product owner (tag them) if scope affects roadmap.
- Architectural changes: Open a Proposal Issue using label `architecture` before implementation.

---

## Branching Model
Recommended model (adapt if org standard differs):
- Default branch: `main` (production-ready).
- Integration branch: `development` (aggregate of next release work). Create it if not present.
- Prefixes:
	- `feat/<short-scope>`
	- `fix/<issue-id>-<short-scope>`
	- `chore/<task>`
	- `docs/<topic>`
	- `refactor/<area>`
	- `release/<version>` (temporary for preparing tagged release)

Delete merged feature branches (server-side or via PR setting) to keep repo clean.

---

## Issue Workflow
1. Search existing issues to avoid duplicates.
2. If new: open an issue using template (add one later if missing) with:
	 - Summary
	 - Motivation / Business Value
	 - Acceptance Criteria (Given / When / Then optional)
	 - Definition of Done items
3. Add appropriate labels: `bug`, `enhancement`, `documentation`, `security`, `architecture`, `good first issue`.
4. Maintainer triages: assigns priority (`P1`, `P2`, `P3`), milestone, and owner.
5. Link PRs to issues using `Fixes #<issue-number>` in description.

For questions use Discussions (if enabled) or prefix issue title with `[Question]`.

---

## Commit Convention (Conventional Commits)
Format: `type(scope): short description`

Types:
`feat` | `fix` | `docs` | `style` | `refactor` | `perf` | `test` | `build` | `ci` | `chore` | `revert`

Examples:
`feat(nav): add sticky header on scroll`
`fix(contact-form): correct email validation logic`
`chore(deps): bump dependency XYZ to 2.3.1`

Rules:
- Use imperative mood (“add”, not “adds”).
- Keep summary <= 72 characters.
- Body (optional): wrap at ~100 chars, explains rationale.
- Footer: reference issues or BREAKING CHANGE notes.

Breaking changes:
```
feat(api)!: remove deprecated endpoint

BREAKING CHANGE: /v1/legacy removed; use /v2/new.
```

---

## Pull Request Guidelines
Checklist (add as a PR template in `.github/pull_request_template.md`):
- [ ] Linked issue (`Fixes #123`) or rationale provided.
- [ ] Tests added/updated or explanation why not applicable.
- [ ] Documentation updated (README / docs/ file / inline).
- [ ] No unresolved TODO comments remain (or tracked in issue).
- [ ] Follows code style & linter output clean.
- [ ] Includes screenshot / recording for UI changes.
- [ ] Changelog updated (see Changelog Management) if user-visible change.

Review Guidelines:
- Keep PRs small & focused (< ~400 lines diff when feasible).
- Squash merge recommended to maintain clean history; use commit message summarizing scope.
- If using merge commits (policy choice), ensure meaningful merge messages.

Draft PRs: Open early for feedback with prefix `WIP:` or mark as Draft. Convert to Ready when stable.

---

## Code Style & Tooling
Because this is a template, tooling is minimal initially. When instantiated, define and document:
- Formatter: `<FORMATTER_CHOICE>` (e.g. Prettier) with config file.
- Linter: `<LINTER_CHOICE>` (e.g. ESLint / Stylelint) with rule profile.
- Style guide reference: `<STYLE_GUIDE_LINK>` if applicable.

Add a section here describing required Node/Runtime versions once set (e.g. "Requires Node 20.x"). Put tooling setup in `package.json` or equivalent.

---

## Testing Guidelines
Placeholder pending test framework selection. When adding tests specify:
- Framework: `<TEST_FRAMEWORK>` (e.g. Vitest, Jest, Playwright, Cypress)
- Command: `npm test` or other.
- Coverage threshold target: `<COVERAGE_THRESHOLD>%`.
- Test directory convention (e.g. `__tests__/` or colocated `*.test.ts`).

Add guidance:
- Unit tests for pure logic.
- Integration tests for cross-module boundaries.
- E2E tests for critical user journeys (deployment pipeline gating).

---

## Documentation Standards
- Keep public-facing docs in `README.md` (high-level) and deeper procedural docs under `docs/`.
- Include architecture diagrams (plantuml / mermaid) in `docs/` where helpful.
- Update `docs/deployment-process.md` when deployment steps or environments change.
- For new environment variables: update a `.env.example` (to be added) and reference them in docs.

---

## Dependency Management
- Pin or lock versions (lockfile committed) to ensure reproducible builds.
- Prefer smaller, well-maintained libraries. Evaluate security posture.
- Periodic audit: `npm audit` / `yarn audit` / `pnpm audit` or language equivalent.
- For upgrades, group related changes; test thoroughly; update changelog.

---

## Security & Responsible Disclosure
See `SECURITY.md` for vulnerability reporting. Do NOT open a public issue for sensitive findings. Email `<SECURITY_CONTACT_EMAIL>`.

Add a Dependabot / Renovate config when the stack is finalized.

---

## Releases & Versioning
- Use Semantic Versioning: MAJOR.MINOR.PATCH.
- Tag format: `v<version>` (e.g. `v1.2.0`).
- Pre-releases: `v1.3.0-beta.1` for testing.
- Release Branch Flow:
	1. Branch from `development` -> `release/<version>`
	2. Update changelog & version metadata (e.g. `package.json` / `app manifest`).
	3. Run final QA.
	4. Merge into `main` (fast-forward or squash) and tag.
	5. Merge `main` back into `development` to keep histories aligned.

Automations (add later): GitHub Actions for tagging, changelog generation, deployment.

---

## Changelog Management
Use `CHANGELOG.md` following [Keep a Changelog](https://keepachangelog.com/en/1.1.0/) structure:
```
## [Unreleased]
### Added
- <entry>
### Changed
- <entry>
### Deprecated
### Removed
### Fixed
### Security
```

Each PR that changes user-visible behavior should add an entry under Unreleased. During release preparation move entries to a new version section with date.

Optionally automate via a tool like `changesets`, `semantic-release`, or `auto-changelog` once stack decided.

---

## Infrastructure / Deployment (Template Notes)
Deployment details belong in `docs/deployment-process.md`. When instantiated, document:
- Environments: `<ENVIRONMENTS_LIST>` (e.g. dev, staging, prod) and their URLs.
- Deployment mechanism: `<DEPLOY_METHOD>` (e.g. GitHub Actions -> Vercel / Netlify / Docker to ECS / etc.).
- Rollback procedure.
- Secrets management approach.

---

## Template Consumer Customization Checklist
When you clone this template to start a real project, perform these steps FIRST:
1. Replace all placeholders `<PROJECT_NAME>`, `<ORG_NAME>`, `<PRODUCT_OWNER_NAME>`, etc.
2. Update `README.md` with real description, tech stack, architecture, maintenance status.
3. Decide & configure runtime stack (e.g. Node version) and add `.nvmrc` / `.tool-versions` if desired.
4. Add linting & formatting configs; update this guide's Code Style section accordingly.
5. Choose test frameworks and create initial test harness + update Testing section.
6. Add CI workflows (`.github/workflows/ci.yml`) for lint, test, build, and (optionally) deploy.
7. Configure security automation (Dependabot / Renovate) & add badges.
8. Add PR / Issue templates under `.github/`.
9. Define initial version (`v0.1.0`) and populate `CHANGELOG.md`.
10. Confirm license (currently `LICENSE` file) matches organizational policy.
11. Add `.env.example` with non-secret placeholders.
12. Update `SECURITY.md` with correct contact paths if needed.
13. Validate branch protection rules (require status checks, linear history, signed commits optional).
14. Remove any unused placeholder docs or sections not relevant.

---

## FAQ
Q: Why so many placeholders?
A: To keep this template agnostic and adaptable to various organizational standards.

Q: Can we simplify guidelines for a very small project?
A: Absolutely—prune sections that add overhead (e.g. architecture proposals) while keeping core hygiene (lint, test, security).

Q: Do I have to use Conventional Commits?
A: Recommended for automated changelog + release tooling; you may adapt to org standard if different.

---

## Attribution
Inspired by industry best practices (Keep a Changelog, Conventional Commits, Open Source Guides). Customize freely.

---

Questions? Open an issue with the label `question` or contact `<PROJECT_CONTACT_EMAIL>`.

<!-- End of Template Contributing Guide -->

