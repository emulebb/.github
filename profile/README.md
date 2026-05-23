# eMule broadband edition

[![Fast Harness CI](https://github.com/emulebb/emulebb-build-tests/actions/workflows/fast-harness-ci.yml/badge.svg)](https://github.com/emulebb/emulebb-build-tests/actions/workflows/fast-harness-ci.yml)

The `emulebb` organization builds eMuleBB, a modern broadband-focused edition
of the classic eMule client, plus adjacent tools for testing, automation,
servers, and P2P workflows around that ecosystem.

eMule broadband edition, compactly known as eMuleBB, is a modern Windows line
for power users with fast upload links, large shared libraries, and trusted
local automation.

It keeps the familiar stock eD2K/Kad protocol and desktop workflow: servers,
Kad search, shared files, upload queues, categories, known clients, and
long-running desktop control. Around that foundation it adds broadband-aware
upload policy, safer large-library operation, authenticated REST automation,
and inspectable release validation without creating an incompatible network
fork.

The first beta release line is planned as **0.7.3**. It is **not yet released**.

## At A Glance

| Area | Current public status |
| --- | --- |
| Release | First beta line `0.7.3`, planned and not yet released |
| Platform | Windows desktop client, with x64 and ARM64 package proof in scope |
| Network | Stock-compatible eD2K and Kad behavior remains the default |
| Automation | Authenticated JSON REST API under `/api/v1` from the existing WebServer |
| Focus | Broadband upload control, large libraries, automated testing, controller integration, and release evidence |

## eMuleBB Ecosystem

eMuleBB is the anchor product. The surrounding repositories form the eMuleBB
ecosystem: reproducible builds, shared test harnesses, public docs, ED2K server
components, controller workflows, and adjacent headless P2P tools that can share
contracts without becoming part of the desktop app.

The goal is not to create an incompatible network fork or a generic P2P lab.
The organization stays centered on practical broadband eMule use: desktop
sharing, large libraries, upload behavior, Kad/eD2K compatibility, local
automation, and evidence-backed releases.

## Testing And Performance Proof

eMuleBB is being built as a tested desktop product, not just a patched source
tree. Public messaging stays tied to the same evidence model used for the beta
release work: fast hosted CI, local native tests, REST/controller checks, UI and
resource proof, live eD2K/Kad scenarios, package provenance, and explicit
operator gates.

The public fast lane runs in GitHub Actions for every push and pull request to
[`emulebb-build-tests`](https://github.com/emulebb/emulebb-build-tests). It installs
the shared Python harness and runs the default fast pytest suite, while the full
release campaign adds the desktop-native, live-network, controller, packaging,
and language/resource checks that do not belong in a small hosted lane.

Performance work is treated the same way: claims are tied to concrete operating
surfaces such as broadband upload slots, modern queue/source/socket/file-buffer
defaults, large shared-library startup behavior, long-path readiness, REST
controller reliability, and x64/ARM64 package proof. The goal is practical
throughput and responsiveness for long Windows sessions while keeping stock
eD2K/Kad compatibility as the boundary.

## Quick Links

| Start here | Link |
| --- | --- |
| Website | [`emulebb.github.io`](https://emulebb.github.io/) |
| Community | [`Discord`](https://discord.gg/uWQa9g37) |
| Source | [`emulebb`](https://github.com/emulebb/emulebb) |
| User docs | [`Product guide`](https://github.com/emulebb/emulebb-tooling/blob/main/docs/reference/GUIDE-EMULEBB.md) |
| Developer docs | [`Development guide`](https://github.com/emulebb/emulebb-tooling/blob/main/docs/reference/DEVELOPMENT-GUIDE.md) |
| Release status | [`0.7.3 dashboard`](https://github.com/emulebb/emulebb-tooling/blob/main/docs/active/RELEASE-0.7.3.md) |

## Start Here

- New users: read the [`Product guide`](https://github.com/emulebb/emulebb-tooling/blob/main/docs/reference/GUIDE-EMULEBB.md) and [`Setup guide`](https://github.com/emulebb/emulebb-tooling/blob/main/docs/reference/GUIDE-SETUP.md).
- Developers: start from [`emulebb`](https://github.com/emulebb/emulebb), the [`emulebb-build`](https://github.com/emulebb/emulebb-build) orchestration repo, and the [`Development guide`](https://github.com/emulebb/emulebb-tooling/blob/main/docs/reference/DEVELOPMENT-GUIDE.md).
- Controller authors: use the [`REST API contract`](https://github.com/emulebb/emulebb-tooling/blob/main/docs/rest/REST-API-CONTRACT.md) and adapter contracts.
- Community discussion: join [`Discord`](https://discord.gg/uWQa9g37).

## What eMuleBB Adds

- Broadband-aware upload slots and queue controls for faster modern links.
- Safer operation with large shared libraries and long-running desktop sessions.
- VPN/interface binding, UPnP/NAT, and WebServer exposure behavior kept under test.
- Authenticated REST automation for trusted local controllers and Arr-style adapters.
- Kad, peer, WebServer, and malformed-request hardening without protocol drift.
- Release evidence that covers native tests, UI automation, REST checks, and live eD2K/Kad scenarios.

## Capability Highlights

### Network Binding And VPN-Aware Operation

- named interface binding for IPv4-capable adapters
- explicit separation between interface targets and address overrides
- live validation profiles that bind the P2P stack through a VPN interface
- WebServer/REST exposure controlled by existing bind, HTTPS, and allowed-IP behavior
- external VPN kill-switch design kept separate from the app instead of being over-claimed as built in

### Modern Performance Defaults

- higher half-open and connection burst defaults for modern Windows
- higher per-client upload cap for broadband slots
- larger UDP receive and TCP send buffers
- SSD/NVMe-friendly file buffering defaults
- larger queue and source limits for busy sessions
- shorter, fixed timeout defaults where old values were too conservative
- advanced Tweaks exposure for important fixed limits

### Broadband Upload Control

- configured upload slot target instead of legacy high-slot drift
- finite upload budget model for modern broadband links
- weak-slot recycling with warm-up, cooldown, and queue refill behavior
- session transfer and session time rotation controls
- large socket send buffer and disk prefetch behavior tied to slot targets

### Seeder And Queue Tools

- all-time and session ratio readouts for shared files and upload decisions
- low-ratio file boost controls for stricter seeding
- optional LowID score deboosting
- cooldown visibility in upload and queue lists
- upload queue actions exposed through desktop and REST-oriented workflows

### Large Library Operation

- recursive share sync work
- startup cache and known.met lookup improvements
- long-path guidance and follow-up work for deep Windows libraries
- stable sorting and large-tree UI responsiveness work
- share-ignore and filename hygiene tracked as product behavior

### Kad And Peer Hardening

- SafeKad and FastKad work in the current Kad paths
- Kad identity tracking and bad-node handling without protocol incompatibility
- bounded cleanup for long-running Kad state
- response-time sampling for Kad timeout behavior
- standalone TCP error-flood protection for pre-handshake abuse
- peer friend, ban, unban, source, upload, and queue operations exposed through REST

### NAT, UPnP, And Exposure Controls

- UPnP/NAT mapping behavior kept in release validation
- PCP/NAT-PMP backend work tracked in the current code line
- WebServer HTTPS and allowed-IP behavior inherited by REST
- bind-policy and socket adversity gates included in beta proof
- no weakening of native eMule exposure rules for controller adapters

### REST And Controller Integration

eMuleBB exposes an authenticated JSON REST API from the existing WebServer
listener for trusted local controllers. The `/api/v1` surface is designed around
native eMule behavior, not a generic downloader model.

Covered areas include:

- transfers and transfer details
- searches and search-result downloads
- servers and Kad controls
- shared files and shared directories
- uploads and upload queue actions
- categories, logs, statistics, preferences, and app status
- qBittorrent-compatible subset routes where Arr clients need them
- Torznab-compatible search adapter behavior for Prowlarr

The controller direction includes aMuTorrent-style workflows and practical
Prowlarr, Radarr, and Sonarr validation lanes while keeping the native desktop
app in charge.

### Release-Grade Validation

The workspace is built around evidence, not guesswork:

- native tests
- Python harnesses
- REST contract and smoke checks
- UI automation
- live eD2K/Kad scenarios
- aMuTorrent and Arr integration validation
- malformed request and WebServer hardening checks
- network socket, UDP, WebSocket, HTTPS, bind-policy, and NAT adversity gates
- x64 and ARM64 package rehearsal evidence before public tagging

## Current Release Focus

- prepare the first beta, `0.7.3`
- keep public release status honest until the beta gates are complete
- finish REST completeness and typed error behavior
- validate UI, REST, eD2K/Kad, and controller scenarios
- keep VPN/interface binding, NAT, and WebServer exposure behavior tested
- improve user-facing setup, tuning, automation, and troubleshooting docs

## Documentation

Start with the public site and the maintained source docs:

- [`emulebb.github.io`](https://emulebb.github.io/) - concise product overview and guide links
- [`Discord`](https://discord.gg/uWQa9g37) - community chat and project discussion
- [`Product guide`](https://github.com/emulebb/emulebb-tooling/blob/main/docs/reference/GUIDE-EMULEBB.md) - setup, tuning, automation, and release-aware use
- [`Development guide`](https://github.com/emulebb/emulebb-tooling/blob/main/docs/reference/DEVELOPMENT-GUIDE.md) - build, validation, CI, packaging, command-line, and recurring guide-refresh workflow
- [`Setup guide`](https://github.com/emulebb/emulebb-tooling/blob/main/docs/reference/GUIDE-SETUP.md) - install model, first-run profile behavior, and startup notes
- [`Network guide`](https://github.com/emulebb/emulebb-tooling/blob/main/docs/reference/GUIDE-NETWORK.md) - eD2K, Kad, binding, UPnP, firewall, and diagnosis
- [`Sharing guide`](https://github.com/emulebb/emulebb-tooling/blob/main/docs/reference/GUIDE-SHARING.md) - shared directories, monitored shares, large libraries, and policy files
- [`Downloads and search guide`](https://github.com/emulebb/emulebb-tooling/blob/main/docs/reference/GUIDE-DOWNLOADS-SEARCH.md) - search modes, result trust, categories, and file workflows
- [`Controllers and REST guide`](https://github.com/emulebb/emulebb-tooling/blob/main/docs/reference/GUIDE-CONTROLLERS-REST.md) - trusted local controllers and automation boundaries
- [`REST API contract`](https://github.com/emulebb/emulebb-tooling/blob/main/docs/rest/REST-API-CONTRACT.md) - authenticated JSON control surface
- [`REST adapter contracts`](https://github.com/emulebb/emulebb-tooling/blob/main/docs/rest/REST-API-ADAPTERS.md) - qBittorrent-compatible and Torznab adapter surface
- [`Troubleshooting guide`](https://github.com/emulebb/emulebb-tooling/blob/main/docs/reference/GUIDE-TROUBLESHOOTING.md) - symptom-led checks for network, sharing, and automation issues
- [`0.7.3 release dashboard`](https://github.com/emulebb/emulebb-tooling/blob/main/docs/active/RELEASE-0.7.3.md) - current planned beta gates, evidence, and readiness rules

## Primary Repositories

- [`emulebb`](https://github.com/emulebb/emulebb) - desktop app and product source
- [`emulebb-setup`](https://github.com/emulebb/emulebb-setup) - reproducible workspace setup
- [`emulebb-build`](https://github.com/emulebb/emulebb-build) - build, validation, and release orchestration
- [`emulebb-build-tests`](https://github.com/emulebb/emulebb-build-tests) - native, Python, UI, REST, and live E2E tests
- [`emulebb-tooling`](https://github.com/emulebb/emulebb-tooling) - roadmap, backlog, policy, audits, and reference docs
- [`emulebb.github.io`](https://emulebb.github.io/) - public product page
- [`goed2k-server`](https://github.com/emulebb/goed2k-server) - ED2K server component for deterministic testing and ecosystem work
- [`amutorrent`](https://github.com/emulebb/amutorrent) - adjacent controller/web workflow product for eMuleBB and aMule-style clients
- [`p2p-overlord-agents`](https://github.com/emulebb/p2p-overlord-agents) and [`p2p-overlord-be`](https://github.com/emulebb/p2p-overlord-be) - adjacent headless/server-oriented P2P tools

## Project Principles

- Keep stock eD2K/Kad protocol compatibility as the default.
- Improve the classic desktop app instead of replacing it with a rewrite.
- Make power-user features observable, testable, and documented.
- Treat REST and controller support as product features.
- Prove behavior with automated and live testing before calling a beta ready.
