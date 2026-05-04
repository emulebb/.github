# eMule broadband edition

eMule broadband edition, compactly known as eMule BB, is a power-user eMule
built for modern Windows, fast connections, large file libraries, and serious
local automation.

It keeps the familiar stock eD2K/Kad protocol and classic eMule workflow:
servers, Kad search, shared files, upload queues, categories, known clients,
and long-running desktop control. Then it pushes that foundation forward with
broadband-aware behavior, safer persistence, a real REST API, reproducible
builds, and live end-to-end testing.

This is no longer just a patched historical branch. eMule broadband edition is
its own product, with its own versioning, release process, roadmap, and
compatibility goals.

## Why eMule BB Exists

eMule BB is for users who still value the classic eMule model, but run it on
modern machines:

- high-bandwidth upload links
- large shared file libraries
- long path Windows filesystems
- always-on desktop sessions
- local controllers and automation
- Arr/aMuTorrent-style integration
- reproducible release validation instead of guesswork

The goal is to keep the stock eD2K/Kad experience useful, controllable, and
trustworthy on current systems, Linux ISOs included.

## What It Focuses On

### Broadband Sharing

eMule BB improves upload and queue behavior for modern broadband use: bounded
upload slot behavior, better queue control, weak-slot recycling, modern defaults,
and sharing controls that make sense for fast connections.

### Large Library Handling

The project has active work around safer shared-file handling, recursive share
sync, startup cache behavior, long-path support, stable sorting, and UI
responsiveness with larger file collections.

### Automation And REST Control

eMule BB includes an authenticated JSON REST API under the existing WebServer
surface. It is designed for trusted local controllers and companion tools that
need to inspect transfers, manage searches, control servers/Kad, read status,
and integrate eMule into a larger local workflow.

### Arr And Controller Integration

The release track includes live testing around Prowlarr, Radarr, Sonarr, and
aMuTorrent-style workflows. The goal is practical integration: search, add,
observe, and control from modern tools without giving up the native desktop app.

### Safer Long-Running Operation

A lot of the work is not flashy, and that is the point: safer file persistence,
better shutdown behavior, reduced stale UI pointers, stronger WebServer
hardening, tighter validation, and fewer silent failure paths.

### Release-Grade Testing

eMule BB is built around a multi-repo validation workspace with native tests,
Python tests, UI automation, REST smoke tests, live eD2K/Kad scenarios, and
live-wire coverage. Releases should be proven, not just compiled.

## Current Release Focus

- Broadband release stabilization.
- REST API completeness and typed error behavior.
- Live E2E coverage for UI, REST, eD2K/Kad, and Arr integration.
- Transfer detail and controller parity for companion apps.
- Cleaner user-facing guides for setup, use, automation, and troubleshooting.

## Primary Repositories

- [`eMule`](https://github.com/eMulebb/eMule) - the desktop app and product source
- [`eMulebb-setup`](https://github.com/eMulebb/eMulebb-setup) - reproducible workspace setup
- [`eMule-build`](https://github.com/eMulebb/eMule-build) - build, validation, and release orchestration
- [`eMule-build-tests`](https://github.com/eMulebb/eMule-build-tests) - native, Python, UI, REST, and live E2E tests
- [`eMule-tooling`](https://github.com/eMulebb/eMule-tooling) - roadmap, backlog, policy, audits, and reference docs

## Project Principles

- Keep stock eD2K/Kad protocol compatibility as the default.
- Prefer practical improvements over rewrite fantasies.
- Make power-user features observable, testable, and documented.
- Treat REST and controller support as product features, not side experiments.
- Prove behavior with automated and live testing before calling it release-ready.

## Status

eMule BB is under active pre-release development. The repositories are public so
the roadmap, release engineering, and compatibility work can be followed as the
project becomes its own product.
