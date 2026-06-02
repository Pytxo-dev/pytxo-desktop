# Pytxo Reality Deck

Passive telemetry UI for [Pytxo](https://github.com/Pytxo-dev/pytxo): run list, wave agents, xterm log stream, and per-agent git diff.

**Requires:** [pytxo](https://github.com/Pytxo-dev/pytxo) **v0.1.x** (pinned via git tag in `src-tauri/Cargo.toml`).

## Prerequisites

- Rust 1.85+
- Node.js 22+
- Pytxo CLI from [pytxo](https://github.com/Pytxo-dev/pytxo): `cargo install --git https://github.com/Pytxo-dev/pytxo --tag v0.1.0 pytxo-cli`

Run the UI from the **same git repository** where you execute `pytxo run`.

## Development

```bash
npm ci
npm run check
cargo build -p pytxo-desktop
```

Tauri dev (from repo root):

```bash
cd src-tauri
cargo tauri dev
```

## Architecture

- Svelte 5 frontend — no direct filesystem access.
- Tauri IPC calls `pytxo-orchestrate` and `pytxo-store` only.

## Screenshot

Add `docs/reality-deck.png` for launch marketing (capture from a three-agent dry run).
