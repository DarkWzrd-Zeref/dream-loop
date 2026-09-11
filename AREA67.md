# AREA 67 overlay for Dream Loop

Upstream skill: [achimala/dream-loop](https://github.com/achimala/dream-loop) (MIT). Written by [@anshuc](https://x.com/anshuc) / Anshu Chimala.
This fork is the AREA 67 owned copy. Keep that attribution on every copy.

Dream Loop is a **process**, not a renderer. Do **not** replace AREA 67 `World3D` with the Vesper / Forgotten Court Three.js demo.

Install from this repo after Skill Altar registration, or keep using `npx skills add achimala/dream-loop` and apply this overlay.

## Mode (do not mix Plus and Pro)

AREA 67 uses **Plus-adapted** only. Do not read `references/pro-mode/workflow.md` for hub work.

| Role | Seat | Job |
| --- | --- | --- |
| Director | Zeref | Art OK / live deploy |
| Manager + critic | grok-heavy | Orchestrate, dream `target.png`, score live vs target |
| Lead coder / worker | cursor-ultra | Close **one** visual gap per pass |
| Target images | Grok Imagine | Exact in-engine screenshot, not concept art |

No Fal / Tripo / Trellis until Zeref gives keys.
No Blender until Claude Friday / keys exist. Do not invent Claude `kind.{sha12}.png` hashes.

Original Plus says the orchestrator should not be a huge model and should spawn worker subagents. AREA 67 maps that to **Heavy orchestrates, Cursor is the worker**. Cursor must not run the Dream Loop skill as if it were both judge and builder.

## Loop

Working files live in the hub repo as `.dream-loop/` (gitignored). Lock `target.png` before coding.

0. Clock in `/mcp/cursor`. `whoami` + `hub_sync`. Report work on `project-area67`.
1. Screenshot **LIVE** campus: https://status-board-production-806b.up.railway.app
2. Heavy dreams `target.png` from **that** screenshot (upgrade graphics, keep layout).
3. Cursor closes **one** visual gap in `bot-ops-status-board`: materials / lighting / sprites / CSS tokens only.
4. Heavy critic vs target, gated rubric: composition 0-3, lighting 0-3, materials 0-3, details 0-1.
5. Zeref OK → live deploy **that slice only**.
6. Repeat one gap at a time. Stop after 3 passes unless Zeref says continue.

If the product already exists, never generate a divergent fantasy scene. Refine the live screenshot.

## First slice

Campus lighting + wet-ground / night glass only. Not 25 new station meshes. Not HUD layout moves.

Allowed paint surfaces (from Heavy reskin spec):

- `src/game/World3D.ts` lights, fog, wet ground
- `src/game/architecture.ts` materials only (keep footprints)
- `src/game/textures.ts` richer tiles, same keys
- `public/sprites/stations/*.png` when files exist
- `src/ui/campus.css` glass / night tokens, do not move layout anchors

## Freeze

Do not edit in a Dream Loop pass:

- `src/content/hubs.json`
- `src/content/agents.json`
- assign / radio / MCP / collision
- `hud.ts` layout anchors
- `kind.{sha12}.png` Claude hashes

Do not deploy AREA 67 from **this** skill repo.

## Night palette (locked unless Heavy revises)

- background `#0b100c`
- fog `#0a140e`
- accent `#76b900` / `#bef264`
- tile-sand `#3a3424` / `#2c271c`
- tile-sand2 `#322c1e` / `#241f16`
- tile-path `#4a4536` / `#353126`
- tile-pad `#3f4a40` / `#2a332c`
- tile-plaza `#2f3830` / `#222a24`
- tile-water `#12301c` / `#0a1c12`
- tile-fence `#1a2218` / `#4a5540`

Look-dev: night classified campus. Gold key from the Well. Teal rim from comms. Glass + stone, not flat boxes. Pals stay readable chips.

## Artist packet

**Task 1 (this repo): none.** Fork/copy does not need art.

**Before visual slice 1, Cursor needs exactly:**

1. `live-campus.png` — screenshot of current live hub (Cursor can capture).
2. `.dream-loop/target.png` — Heavy Imagine upgrade of that shot, same camera/layout.
3. This overlay's night palette unless Heavy issues a replacement.

**Not needed for slice 1:** recut-6 zip, station stills, new meshes, Fal keys, Claude GLB/PNG pack.

## Skill Altar record (Heavy registers)

```json
{
  "id": "dream-loop",
  "title": "Dream Loop",
  "kind": "visual-iteration",
  "source": "https://github.com/achimala/dream-loop",
  "owned": "https://github.com/DarkWzrd-Zeref/dream-loop",
  "method": "screenshot-live → Imagine target → Cursor codes one gap → Heavy critic → live slice"
}
```

## Exit

- Score >= 8 on the current slice and Zeref OK: ship live, stop or start the next gap.
- Same named gap twice: stop and ask Zeref. Do not grind tokens.
