# Mini roadmap

The goal is to evolve the current Patchright-based setup into an automatable
anti-detect browser with a practical UI/UX. This is a direction, not a release
schedule; unchecked items are planned work, not existing features.

## Current foundation

- [x] Chrome sessions powered by Patchright.
- [x] Proxy rotation, parallel sessions, and isolated temporary profiles.
- [x] TypeScript scenario entry points and browser interaction helpers.

## 1. Strengthen the core

- [ ] Validate configuration and proxy input with actionable errors.
- [ ] Make session shutdown and profile cleanup reliable on failure and interruption.
- [ ] Add regression coverage for configuration, proxy parsing, and session lifecycle.

## 2. Add UI/UX

- [ ] Design the main flows: create a profile, assign a proxy, launch, inspect, and stop.
- [ ] Build a dashboard for profiles, proxies, active sessions, status, and sanitized logs.
- [ ] Add persistent profile storage alongside temporary sessions, with explicit deletion.
- [ ] Cover first-run setup, empty/error states, and keyboard-accessible controls.

## 3. Deliver an automatable anti-detect browser

- [ ] Expose profile and session lifecycle through a documented local API and CLI.
- [ ] Allow scripts and agents to launch a selected profile and run reusable scenarios.
- [ ] Add queued runs, concurrency limits, cancellation, and machine-readable results.
- [ ] Protect automation endpoints and stored credentials; document installation and upgrades.
- [ ] Publish reproducible compatibility checks and known detection limitations.

The existing browser/session modules are the starting point. UI technology and
the API contract remain open for proposals. Detection resistance depends on the
browser version and target environment; it is not a guarantee of invisibility.

To help, open a focused proposal using the feature template and follow
[CONTRIBUTING.md](CONTRIBUTING.md).
