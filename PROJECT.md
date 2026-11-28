# Project definition — Sakura Succubus 3 Vita

## Product and boundary
A PS Vita Ren'Py package shell for **Sakura Succubus 3**. It provides Vita metadata, LiveArea assets and install instructions, not the original PC game.

## Upstream and runtime
- Original game: [Sakura Succubus 3 on Steam](https://store.steampowered.com/app/1406020/Sakura_Succubus_3/).
- Runtime/tool lineage: [Ren'Py PSVita Distribution Tool](https://github.com/SonicMastr/renpy-vita).
- The user supplies the original `game/` folder; do not redistribute it.

## Users and target
PS Vita users installing via VitaShell. The README records known glitches in Settings and Load/Save menus while Quick Load/Save is reported to work; those caveats must remain until retested.

## Install contract
The README specifies `ux0:/app/RNPYSSIII/` for original game data. SFO identity must match.

## Architecture and dependencies
Static Vita package shell with SFO, icon/pic, LiveArea XML, background/startup images and docs. Depends on external game data and Ren'Py Vita runtime.

## Security and quality
Run package integrity checks; preserve the known-bug disclosure and avoid asserting fixes without device evidence. Documentation is English.

## Verified baseline
The repository contains Vita package metadata and wiki source, not the full original game. CI can validate file structure but cannot prove menu behaviour.

## Release acceptance
Package metadata and install path agree, source attribution is present, and a Vita test covers boot, Settings, Load/Save, Quick Save/Load, suspend/resume and performance.