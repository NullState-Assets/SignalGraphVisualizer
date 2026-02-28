# SignalGraphVisualizer — Lite

> **Stop fighting your engine. Ship faster.**

---

## The Problem

Signal connections in Godot are invisible. They live in the editor's Node panel, disconnected from the code, and there is no built-in way to see the full picture of what is connected to what at runtime. Debugging a signal that never fires means opening every node one by one and checking its connections manually.

---

## The Solution

Add `script.gd` to any node in your scene. On play, it opens a floating window that scans your entire scene tree and renders a live graph of every signal connection — emitters on the left of each bezier curve, receivers on the right. Pan with middle mouse, zoom with scroll wheel, click any card to highlight its connections.

No plugins. No autoloads. One file.

---

## What's in the Lite Version

- Live runtime scan of all signal connections in the scene tree
- Visual graph with bezier connection lines between node cards
- Cards show each node's emitted and received signals by name
- Click a card to highlight its connected nodes and dim everything else
- Pan (middle mouse) and zoom (scroll wheel) canvas navigation
- Refresh and Reset View toolbar buttons
- Configurable via Inspector: colors, layout, card sizing, zoom limits

## What's in the Full Version

The full version adds a **live filter bar**: type any node name or signal name to instantly hide everything unrelated. On a scene with 40+ nodes and hundreds of connections, the filter is the difference between a usable debugging tool and a visual noise machine. It also adds a **click-to-inspect panel**: click any card to see its full node path, node type, and complete signal list in a pinned side panel — without needing to read the Output log.

**Full version on itch.io:** https://nullstateassets.itch.io

---

## Quick Start

1. Copy `script.gd` into your Godot project.
2. Add it as a child node anywhere in your scene (it spawns its own Window).
3. Hit **Play** — the graph window opens automatically.
4. Press **Refresh** after making signal connection changes.

---

## Compatibility

| Engine    | Language  | Tested On    |
|-----------|-----------|--------------|
| Godot 4.x | GDScript  | 4.2, 4.3     |

---

## License

MIT License. Free for personal and commercial use. Attribution appreciated but not required.
