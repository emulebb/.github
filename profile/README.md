# eMule BB

eMule BB is an independently versioned broadband-focused eD2K/Kad client.

The goal is straightforward: carry the classic eMule workflow forward as its
own product for modern Windows while preserving compatibility with the community
network. The project focuses on careful maintenance, safer persistence, better
high-speed sharing behavior, stronger test coverage, and practical local
automation through the WebServer REST API.

## Mission

- Maintain eMule BB as its own product with its own release versioning.
- Preserve eD2K and Kad interoperability unless a change is explicitly scoped.
- Improve broadband-era defaults, sharing controls, and queue behavior.
- Keep release engineering reproducible through a scripted multi-repo workspace.
- Make REST, live E2E testing, and controller integration first-class release
  gates.

## Primary Repositories

- [`eMule`](https://github.com/eMulebb/eMule) - application source and release branches
- [`eMulebb-setup`](https://github.com/eMulebb/eMulebb-setup) - workspace materialization
- [`eMule-build`](https://github.com/eMulebb/eMule-build) - build and validation orchestration
- [`eMule-build-tests`](https://github.com/eMulebb/eMule-build-tests) - native, Python, UI, REST, and live E2E harnesses
- [`eMule-tooling`](https://github.com/eMulebb/eMule-tooling) - workspace policy, backlog, audits, and reference docs

## Current Focus

- Broadband release stabilization.
- REST API completeness and typed error behavior.
- Live E2E coverage for UI, REST, eD2K/Kad, and Arr integration.
- User-facing release guides and cleaner public documentation.

## Project Principles

- Compatibility first.
- Small reviewed changes over broad rewrites.
- Reproducible workspace setup over machine-local assumptions.
- Tests and live proof before expanding release scope.
