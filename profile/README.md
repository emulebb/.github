# eMuleBB

[![Rust CI](https://github.com/emulebb/emulebb-rust/actions/workflows/ci.yml/badge.svg?branch=main)](https://github.com/emulebb/emulebb-rust/actions/workflows/ci.yml)
[![MFC baseline](https://github.com/emulebb/emulebb/actions/workflows/baseline.yml/badge.svg?branch=main)](https://github.com/emulebb/emulebb/actions/workflows/baseline.yml)
[![Docs](https://github.com/emulebb/emulebb-tooling/actions/workflows/docs-site.yml/badge.svg?branch=main)](https://github.com/emulebb/emulebb-tooling/actions/workflows/docs-site.yml)

eMuleBB is a small eD2K/Kad workshop with two public client lanes:

- **[emulebb-rust](https://github.com/emulebb/emulebb-rust)** is the active
  experimental beta. CI-gated
  [nightly builds](https://github.com/emulebb/emulebb-rust/releases) from
  `main` are the current public testing channel. They are not production-ready.
- **[eMuleBB MFC](https://github.com/emulebb/emulebb)** is the stable Windows
  line. Version
  [`0.7.3`](https://github.com/emulebb/emulebb/releases/tag/emulebb-v0.7.3)
  remains published and the `0.7.x` branch continues as a long-term maintenance
  lane for bugs and bounded, low-risk improvements.

The Rust client is where new product development happens. The MFC client stays
available as a useful, maintained result of the original experiment; it is not
on a broad feature or architecture roadmap.

Rust development is a best-effort, spare-time project. Contributions are very
welcome; start with the
[contributing guide](https://github.com/emulebb/emulebb-rust/blob/main/CONTRIBUTING.md).

## Repository Status

| Repository | Role |
| --- | --- |
| [`emulebb-rust`](https://github.com/emulebb/emulebb-rust) | Active experimental beta; nightly public testing and current product-development lane |
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

The two current public entry points are the Rust nightly beta channel and the
stable MFC release. Rust nightlies are unsigned experimental builds; use the
published `SHA256SUMS` and provenance attestations when testing them. The MFC
`0.7.3` release also preserves the historical **eMuleBB Suite** installer and
matching aMuTorrent artifact. “Suite” describes that shipped bundle; it is not
the name of an active cross-client product roadmap.

Native Windows VPN integration and BitTorrent companion work are not current
priorities. Deployment-specific container or VPN stacks should be evaluated on
their own evidence rather than inferred from these repositories.

## Start Here

- [Get the Rust nightly builds](https://github.com/emulebb/emulebb-rust/releases)
- [Contribute to emulebb-rust](https://github.com/emulebb/emulebb-rust/blob/main/CONTRIBUTING.md)
- [Download eMuleBB MFC 0.7.3](https://github.com/emulebb/emulebb/releases/tag/emulebb-v0.7.3)
- [Read the public documentation](https://emulebb.github.io/emulebb-tooling/)
- [Review the eMuleBB Roadmap](https://github.com/orgs/emulebb/projects/3)
- [Open the organization website](https://emulebb.github.io/)

Please report issues in the repository that owns the affected code. Paused and
frozen experiments may not accept new issues; their histories remain available
for reference.
