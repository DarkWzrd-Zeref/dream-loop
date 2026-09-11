# AREA 67 overlay for Dream Loop

Upstream skill: [achimala/dream-loop](https://github.com/achimala/dream-loop) (MIT). Written by [@anshuc](https://x.com/anshuc) / Anshu Chimala.
This fork is the AREA 67 owned copy. Keep that attribution on every copy.

Dream Loop is a **process**, not a renderer. Do **not** replace AREA 67 `World3D` with the Vesper / Forgotten Court Three.js demo.

## Mode (do not mix Plus and Pro)

AREA 67 uses **Plus-adapted** only. Do not read `references/pro-mode/workflow.md` for hub work.

Zeref 2026-09-11 18:16 ET role flip, updated 18:38 ET:

| Role | Seat | Job |
| --- | --- | --- |
| Director + coder | claude | Slice code. World3D lights/fog/wet ground. Numeric critic. |
| Manager, processor, shipper | cursor-ultra | Clock in, radio, packets, PRs, live ship |
| Artist + critic | grok-heavy | Dream `target.png` from live campus shot, score live vs target, station sprites |
| Target images | Grok Imagine | Exact in-engine screenshot, not concept art |
| Final OK | Zeref | Art OK / live deploy |

No Fal / Tripo / Trellis until Zeref gives keys.
No Blender until Claude Friday / keys exist. Do not invent Claude `kind.{sha12}.png` hashes.

## Loop

Working files live in the hub repo as `.dream-loop/` (gitignored). Lock `target.png` before coding.

0. Cursor clocks `/mcp/cursor`. Claude clocks `/mcp/claude`. Heavy clocks `/mcp/grok-heavy`.
1. Cursor screenshots **LIVE** campus: https://status-board-production-806b.up.railway.app
2. Heavy dreams `target.png` from **that** screenshot (upgrade graphics, keep layout).
3. Cursor posts `CLAUDE-HANDOFF-00N` with exact files, freeze list, and done-when.
4. Claude codes **one** visual gap: materials / lighting / sprites / CSS tokens only. Then stops and radios `HANDOFF-BACK`.
5. Cursor reviews, processes, opens PR, asks Heavy critic.
6. Zeref OK → Cursor ships that slice live.
7. Repeat one gap at a time. Stop after 3 passes unless Zeref says continue.

If the product already exists, never generate a divergent fantasy scene. Refine the live screenshot.

## First slice (after skill lock + handoff)

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

## Night palette (H4 — measured from Heavy 25 stills, 2026-09-11)

Claude hue census on the Imagine set. This replaces the old `#0b100c` green-black block, which oversold lime ~20x.

- background `#000000` pure black void. No sky, no horizon, no haze, no blue-hour panorama.
- stone mid `#1c2328` to `#2d2e30` desaturated cool grey
- highlight mean `#8f7c67` warm
- hue budget of saturated pixels:
  - amber / orange 15–45deg ~69%
  - cool blue 210–225deg ~17%
  - lime 105–120deg ~3.5% MAX
- lime is ACCENT ONLY: Well ring, Altar runes, Spector scan. Never ambient, never ground.
- signature: wet stone, vertical specular streaks under every practical, shallow puddles, near-zero ambient fill so geometry reads by highlight not fill.

Live 1.4.1 gap (Claude critic, campus only, HUD excluded): amber 0.0% vs 69.3% target. HemisphereLight 2.1 floods teal. That is the slice to close.

Deprecated (do not code to these):

- `#0b100c` / `#0a140e` green-black
- lime as ambient `#76b900` / `#bef264`
- Codex blue-hour panorama `/environments/area67-bluehour-panorama.png`

## Skill lock

Repo: https://github.com/DarkWzrd-Zeref/dream-loop
Claude packet: [packets/A67-DREAMLOOP-CLAUDE.json](packets/A67-DREAMLOOP-CLAUDE.json)
Altar record: [packets/SKILL-ALTAR.json](packets/SKILL-ALTAR.json)

Skill Altar write from grok-heavy is locked (needs seat Bearer). Cursor or operator can stamp.

## Exit

- Score >= 8 on the current slice and Zeref OK: Cursor ships live, stop or start the next gap.
- Same named gap twice: stop and ask Zeref. Do not grind tokens.
