# eMuleBB

[![Rust CI](https://github.com/emulebb/emulebb-rust/actions/workflows/ci.yml/badge.svg?branch=main)](https://github.com/emulebb/emulebb-rust/actions/workflows/ci.yml)
[![MFC baseline](https://github.com/emulebb/emulebb/actions/workflows/baseline.yml/badge.svg?branch=main)](https://github.com/emulebb/emulebb/actions/workflows/baseline.yml)
[![Docs](https://github.com/emulebb/emulebb-tooling/actions/workflows/docs-site.yml/badge.svg?branch=main)](https://github.com/emulebb/emulebb-tooling/actions/workflows/docs-site.yml)

eMuleBB is a small eD2K/Kad workshop with two public client lanes:

- **[emulebb-rust](https://github.com/emulebb/emulebb-rust)** is the active
  experimental beta. The first public beta,
  [`rust-v0.1.0-beta.1`](https://github.com/emulebb/emulebb-rust/releases/tag/rust-v0.1.0-beta.1),
  is available for testing. It is not yet a production-ready client.
- **[eMuleBB MFC](https://github.com/emulebb/emulebb)** is the stable Windows
  line. Version
  [`0.7.3`](https://github.com/emulebb/emulebb/releases/tag/emulebb-v0.7.3)
  remains published and the `0.7.x` branch continues as a long-term maintenance
  lane for bugs and bounded, low-risk improvements.

The Rust client is where new product development happens. The MFC client stays
available as a useful, maintained result of the original experiment; it is not
on a broad feature or architecture roadmap.

## Repository Status

| Repository | Role |
| --- | --- |
| [`emulebb-rust`](https://github.com/emulebb/emulebb-rust) | Active experimental beta; current product-development lane |
| [`emulebb`](https://github.com/emulebb/emulebb) | Stable `0.7.x` Windows client; long-term maintenance |
| [`emulebb-tooling`](https://github.com/emulebb/emulebb-tooling) | Public roadmap, lifecycle policy, product docs, and engineering references |
| [`emulebb-build`](https://github.com/emulebb/emulebb-build) | Workspace, build, validation, and packaging orchestration |
| [`emulebb-build-tests`](https://github.com/emulebb/emulebb-build-tests) | Shared test and live-network harness |
| [`goed2k-server`](https://github.com/emulebb/goed2k-server) | Fixed-purpose eD2K test harness server; no product evolution planned |
| [`ed2k-server`](https://github.com/emulebb/ed2k-server) | Reference fork retained for analysis and possible upstream contributions |
| [`amule`](https://github.com/emulebb/amule) | aMule fork retained mainly for source analysis and build comparison |
| [`amutorrent`](https://github.com/emulebb/amutorrent) | Frozen controller fork formerly shipped with the MFC `0.7.3` bundle |
| [`qbittorrentbb`](https://github.com/emulebb/qbittorrentbb) | Paused experiment; public for reference, with no active roadmap |
| [`emulebb-libtorrent`](https://github.com/emulebb/emulebb-libtorrent) | Paused dependency fork associated with qBittorrentBB |

TrackMuleBB was an exploratory private controller project and is archived.

## Releases And Historical Bundles

The two current public entry points are the Rust beta and the stable MFC
release. The MFC `0.7.3` release also preserves the historical **eMuleBB Suite**
installer and matching aMuTorrent artifact. “Suite” describes that shipped
bundle; it is not the name of an active cross-client product roadmap.

Native Windows VPN integration and BitTorrent companion work are not current
priorities. Deployment-specific container or VPN stacks should be evaluated on
their own evidence rather than inferred from these repositories.

## Start Here

- [Try the Rust beta](https://github.com/emulebb/emulebb-rust/releases/tag/rust-v0.1.0-beta.1)
- [Download eMuleBB MFC 0.7.3](https://github.com/emulebb/emulebb/releases/tag/emulebb-v0.7.3)
- [Read the public documentation](https://emulebb.github.io/emulebb-tooling/)
- [Review the eMuleBB Roadmap](https://github.com/orgs/emulebb/projects/3)
- [Open the organization website](https://emulebb.github.io/)

Please report issues in the repository that owns the affected code. Paused and
frozen experiments may not accept new issues; their histories remain available
for reference.
