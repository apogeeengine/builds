# Apogee Engine builds

Public build pipeline for the [Apogee Engine](https://github.com/apogeeengine) (the engine's source is private). The
`Build` workflow checks it out with a read-only deploy key and builds, on this repo's free runners:

| Artifact | What it is |
|---|---|
| `apogee-<platform>-editor-<arch>` | The editor: it makes games and mods (Project > Pack Mod...) and exports games |
| `apogee-<platform>-template_release-<arch>`, `template_debug` | The export templates |

Platforms: `linuxbsd`, `windows`, `macos` (universal). Run the workflow with an engine ref; with a tag it publishes the
binaries as a release. OpenAL Soft and `steam_api` come beside the binaries (Valve's headers and import libraries are
never published).
