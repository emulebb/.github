# eMule broadband edition

eMule broadband edition, compactly known as eMule BB, is a power-user eMule
line for modern Windows systems, fast upload links, large shared libraries, and
trusted local automation.

It keeps the familiar stock eD2K/Kad protocol and classic eMule workflow:
servers, Kad search, shared files, upload queues, categories, known clients,
and long-running desktop control. Around that foundation it adds broadband-aware
upload policy, safer large-library operation, authenticated REST automation, and
release validation that can be inspected.

The first beta release line is planned as **0.7.3**. It is **not yet released**.

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

eMule BB exposes an authenticated JSON REST API from the existing WebServer
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
- [`Product guide`](https://github.com/eMulebb/eMule-tooling/blob/main/docs/reference/GUIDE-EMULEBB.md) - setup, tuning, automation, and release-aware use
- [`Setup guide`](https://github.com/eMulebb/eMule-tooling/blob/main/docs/reference/GUIDE-SETUP.md) - install model, first-run profile behavior, and startup notes
- [`Network guide`](https://github.com/eMulebb/eMule-tooling/blob/main/docs/reference/GUIDE-NETWORK.md) - eD2K, Kad, binding, UPnP, firewall, and diagnosis
- [`Sharing guide`](https://github.com/eMulebb/eMule-tooling/blob/main/docs/reference/GUIDE-SHARING.md) - shared directories, monitored shares, large libraries, and policy files
- [`Downloads and search guide`](https://github.com/eMulebb/eMule-tooling/blob/main/docs/reference/GUIDE-DOWNLOADS-SEARCH.md) - search modes, result trust, categories, and file workflows
- [`Controllers and REST guide`](https://github.com/eMulebb/eMule-tooling/blob/main/docs/reference/GUIDE-CONTROLLERS-REST.md) - trusted local controllers and automation boundaries
- [`REST API contract`](https://github.com/eMulebb/eMule-tooling/blob/main/docs/rest/REST-API-CONTRACT.md) - authenticated JSON control surface
- [`REST adapter contracts`](https://github.com/eMulebb/eMule-tooling/blob/main/docs/rest/REST-API-ADAPTERS.md) - qBittorrent-compatible and Torznab adapter surface
- [`Troubleshooting guide`](https://github.com/eMulebb/eMule-tooling/blob/main/docs/reference/GUIDE-TROUBLESHOOTING.md) - symptom-led checks for network, sharing, and automation issues
- [`0.7.3 release dashboard`](https://github.com/eMulebb/eMule-tooling/blob/main/docs/active/RELEASE-0.7.3.md) - current planned beta gates, evidence, and readiness rules

## Primary Repositories

- [`eMule`](https://github.com/eMulebb/eMule) - desktop app and product source
- [`eMulebb-setup`](https://github.com/eMulebb/eMulebb-setup) - reproducible workspace setup
- [`eMule-build`](https://github.com/eMulebb/eMule-build) - build, validation, and release orchestration
- [`eMule-build-tests`](https://github.com/eMulebb/eMule-build-tests) - native, Python, UI, REST, and live E2E tests
- [`eMule-tooling`](https://github.com/eMulebb/eMule-tooling) - roadmap, backlog, policy, audits, and reference docs
- [`emulebb.github.io`](https://emulebb.github.io/) - public product page

## Project Principles

- Keep stock eD2K/Kad protocol compatibility as the default.
- Improve the classic desktop app instead of replacing it with a rewrite.
- Make power-user features observable, testable, and documented.
- Treat REST and controller support as product features.
- Prove behavior with automated and live testing before calling a beta ready.
