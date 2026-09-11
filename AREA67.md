# AREA 67 overlay for Dream Loop

Upstream skill: [achimala/dream-loop](https://github.com/achimala/dream-loop) (MIT). Written by [@anshuc](https://x.com/anshuc) / Anshu Chimala.
This fork is the AREA 67 owned copy. Keep that attribution on every copy.

Dream Loop is a **process**, not a renderer. Do **not** replace AREA 67 `World3D` with the Vesper / Forgotten Court Three.js demo.

## Mode (do not mix Plus and Pro)

AREA 67 uses **Plus-adapted** only. Do not read `references/pro-mode/workflow.md` for hub work.

Zeref 2026-09-11 18:16 ET role flip:

| Role | Seat | Job |
| --- | --- | --- |
| Director | Zeref | Art OK / live deploy |
| Manager, processor, shipper | cursor-ultra | Clock in, radio, packets, critic handoff, PRs, live ship |
| Artist + critic | grok-heavy | Dream `target.png`, score live vs target |
| Coder | claude | **Code only.** One visual gap per handoff. No radio strategy, no deploy, no skill register |
| Target images | Grok Imagine | Exact in-engine screenshot, not concept art |

No Fal / Tripo / Trellis until Zeref gives keys.
No Blender until Claude Friday / keys exist. Do not invent Claude `kind.{sha12}.png` hashes.

Claude never runs Dream Loop as judge + builder. Cursor never writes the slice. Heavy never merges.

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

## Skill lock

Repo: https://github.com/DarkWzrd-Zeref/dream-loop
Claude packet: [packets/A67-DREAMLOOP-CLAUDE.json](packets/A67-DREAMLOOP-CLAUDE.json)
Altar record: [packets/SKILL-ALTAR.json](packets/SKILL-ALTAR.json)

## Exit

- Score >= 8 on the current slice and Zeref OK: Cursor ships live, stop or start the next gap.
- Same named gap twice: stop and ask Zeref. Do not grind tokens.
