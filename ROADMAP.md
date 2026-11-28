# Roadmap — Sakura Succubus III Vita port

## P0 — Preserve package identity
- [x] Track Vita SFO metadata and LiveArea assets.
- [x] Document the upstream game source and separate user-supplied game files.
- [ ] Reconcile the published VPK with tracked RNPYSSIII metadata and record its SHA-256.

## P1 — Package integrity
- [x] Add an offline SFO parser regression test with bounds checks.
- [x] Verify title ID, category, title and application version in CI.
- [x] Verify required PNG assets and parse the LiveArea XML.
- [x] Fail if an original game/ payload is accidentally committed.
- [ ] Pin the exact Ren'Py Vita runtime/tool revision in a reproducible build recipe.

## P2 — Runtime qualification
- [ ] Install on a physical PS Vita and record firmware, storage layout and free space.
- [ ] Verify first boot, game-file discovery, save/load, audio, suspend/resume and repeated launch.
- [ ] Re-test the known Settings and Load/Save menu glitches; record whether Quick Save/Load remains reliable.

## P3 — Maintenance release
- [ ] Rebuild from a documented input game build and pinned runtime.
- [ ] Compare generated package metadata and asset hashes against the reviewed baseline.
- [ ] Publish notes and checksums only after physical-device qualification.

## Acceptance
CI passes; the SFO identity remains RNPYSSIII; no original game payload is tracked; LiveArea assets are valid; and any release candidate has a separate physical Vita report. CI is not hardware certification.

## Release target
Maintain the existing 1.40 port version; no release or version bump is proposed by this change.


## Additional automated gate — 2026-11-28

The integrity suite now checks that the LiveArea `image` and `startup-image`
references are unique plain filenames confined to `sce_sys/livearea/contents`.
It also verifies the PNG signature, IHDR marker and non-zero dimensions for
`icon0.png`, `pic0.png`, the LiveArea background and startup image.

These checks validate package structure only. They do not prove visual quality,
controller behaviour, runtime boot or gameplay on a physical Vita.
