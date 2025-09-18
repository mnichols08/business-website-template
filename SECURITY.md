# Security Policy

## Supported Versions
This template is in an early research / development phase. Only the `development` (once created) and the most recent tagged release are intended to receive security-related fixes. During the current phase, fixes will typically land on the active development branch.

| Version / Branch | Supported | Notes |
|------------------|-----------|-------|
| Unreleased `development` | Yes (best effort) | Active iteration branch.
| Future `main` (after stabilization) | Yes | Stable, production-ready baseline.
| Older tags | No | Please update to the latest tag.

## Reporting a Vulnerability
Please DO NOT open a public GitHub issue for security vulnerabilities.

Instead, report privately via email:

`security@PLACEHOLDER-DOMAIN` (replace with your preferred contact email before broad distribution or client use)

When reporting, include (as available):
- Description of the issue
- Steps to reproduce / proof-of-concept
- Potential impact / severity
- Suggested remediation (if known)
- Any relevant environment details

You will receive an acknowledgment within 5 business days (adjust this SLA as appropriate for your workflow).

## Disclosure Process
1. Report received and acknowledged.
2. Triage & reproduce.
3. Assign severity and plan remediation timeline.
4. Develop and test a fix.
5. Prepare coordinated release (may include a security advisory & CVE request if warranted).
6. Publish fix and notify reporter (and optionally credit them if requested and appropriate).

## Preferred Formats
- Simple text description is fine.
- Provide minimized repro cases (avoid sending large archives where possible).
- Avoid including exploit payloads that could trigger security tools; reference them descriptively if sensitive.

## Out of Scope (Examples)
- Dependency advisories already published upstream unless a direct exploitable path is demonstrated in this template.
- Social engineering attacks.
- Non-production configuration weaknesses that require privileged repository access.

## Hardening Recommendations (For Derived Projects)
When using this template for client projects, consider:
- Enabling Dependabot (security & version updates)
- Adding a Software Bill of Materials (SBOM) generation step
- Enforcing branch protection and required reviews
- Adding CI security scanners (SAST/Dependency/Secret scanning)

## Questions
For general (non-sensitive) questions, use a standard issue instead of the security contact.

---
Maintenance Tip: Replace the placeholder email and update support table as the branching model evolves.
