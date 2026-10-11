# RSAngband — Coding Agent Instructions

This repository is based on Angband 4.2.6, written in C.

## Architecture

- Preserve the existing flat, feature-prefixed module organization in `src/`.
- Identify existing naming conventions and subsystem responsibilities before adding new modules.
- Examples include `mon-*` for monsters, `obj-*` for objects, `player-*` for player mechanics, `cave-*` for dungeon state, and `cmd-*` for commands.
- Prefer extending existing modules instead of creating duplicate implementations.
- Follow the existing C coding style, header conventions, and memory-management practices.

## Development workflow

1. Inspect relevant code and its callers before modifying behavior.
2. Explain the current implementation before proposing substantial changes.
3. Keep changes small and focused.
4. Preserve existing game behavior unless a change is explicitly requested.
5. Update or add tests where practical.

## Build environment

- Windows with Visual Studio Build Tools 2026.
- CMake with the Visual Studio 18 2026 generator.
- Target Win32 (x86) because the bundled PNG/zlib libraries are 32-bit.
- Preserve existing build settings.
- Do not treat pre-existing MSVC warnings as new errors.
