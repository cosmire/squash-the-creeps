# Squash the Creeps

A complete 3D platformer-style game in Rust — character controller, jump-to-squash combat, mob spawning, and music, wired through gdext.

A **Cosmire Template** — open source, and verified to build.

## Versions

| | |
|---|---|
| Godot | 4.5.2 |
| Rust | 1.94.0 |
| gdext | `410580d477fe` |

Pinned together as one tested combination, rebuilt weekly by CI. The badge on
this repo reflects a real build, not a claim.

## Get started

Clone it:
```
git clone https://github.com/cosmire/squash-the-creeps.git
cd squash-the-creeps/rust && cargo build
```
Then open the `godot/` folder in Godot 4.5.2.

Or scaffold it under your own name (requires `cargo-generate`):
```
cargo generate --git https://github.com/cosmire/squash-the-creeps.git
```
Both routes produce the same project.

## Renaming it

The project keeps its original name on clone or generate. To rename it, edit
three places:

| File | Change |
|---|---|
| `rust/Cargo.toml` | `name = "squash-the-creeps"` |
| `godot/rust.gdextension` | library filenames — `libsquash_the_creeps.so` and friends |
| `godot/project.godot` | `config/name="Squash the Creeps"` |

The crate name and the library filenames must match, or Godot will not find
the compiled library.

## Layout

- `rust/` — game logic, one module per system
- `godot/` — scenes and assets
- `docs/architecture.md` — why it is shaped this way
- `docs/context.md` — the same, structured for coding agents

## Licensing

Rust source derives from the [godot-rust demo projects](https://github.com/godot-rust/demo-projects)
and is **MPL-2.0**. The Godot project and art derive from Godot's own demo,
**MIT** (Copyright (c) 2017 KidsCanCode). See `LICENSE` and `NOTICE`.

MPL-2.0 is file-level copyleft: modified MPL files stay MPL with source
available. This template may not be relicensed under MIT.
