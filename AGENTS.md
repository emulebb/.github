# Rules

- Read `EMULEBB_WORKSPACE_ROOT\repos\emulebb-tooling\docs\WORKSPACE-POLICY.md`
  first; it is authoritative for workspace-wide rules.
- Start from
  `EMULEBB_WORKSPACE_ROOT\repos\emulebb-tooling\docs\reference\AGENT-CHECKLIST.md`
  for the repeatable operating path.

This repository holds the public GitHub **organization profile** for the eMule
broadband edition org. Its only published artifact is `profile/README.md`, which
GitHub renders on the `emulebb` org landing page. Everything below is this repo's
local deltas only.

## Hard Rules

- The org profile is **text-first**. Do not add screenshots, mascot art, copied
  application artwork, or other brand image assets unless explicitly approved.
- Treat `emulebb-tooling` active/reference docs as the source of truth. The
  profile summarizes and links; it does not invent feature or release facts.
- Only shipped, landed, passed, or release-proven features belong in the public
  profile copy. Keep version and release references in step with the current
  release docs (e.g. the active 0.7.3 RC train).
- Keep English canonical.
- Preserve technical terms such as `eD2K`, `Kad`, `REST`, `JSON`, `API`, `VPN`,
  `UPnP/NAT`, `x64`, `ARM64`, repo names, file paths, URLs, and code identifiers.
- Use granular commits: keep policy, content, and link/badge changes separate.
- Files are UTF-8 with LF endings (`.gitattributes`, `.editorconfig`).
