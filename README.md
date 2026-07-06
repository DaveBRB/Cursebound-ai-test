# Cursebound: Houses of the Ancients — One-Shot Prototype

A playable browser prototype of **Cursebound**, built from the game's Prototype Bible and
Gameplay Design Document. Open-world curse survival, not zombies: every house is both a
loot cache and a cursed crime scene.

**Play it:** open `index.html` in any modern browser. One self-contained file — no
libraries, no external assets, everything drawn with Canvas shapes, text, and glow effects.

**3D version:** open `3d index test 1.html` for a first-person raycast build of the same
game — procedural wall textures, sprite monsters unique to each house, pointer-lock mouse
look, a drawn revolver + torch viewmodel, heartbeat/drone audio, jump scares, film grain,
and a field journal (J). Same rules, scarier room.

## The loop

1. Pick a faction on the title screen (Celtic, Assyrian, or Egyptian — each has a passive).
2. Scavenge the village and enter one of three cursed houses: **Rowan Farm**,
   **Clay Ledger House**, **Widow's Hall**.
3. Touch the **purple** curse object → the house wakes: `DORMANT → OMEN → SEAL → HUNT →
   DISTORTION → JUDGMENT → RESOLVED`.
4. The doors seal. Collect **3 blue clues**, avoid the **red** hunter and the mimic
   teammate, then perform the ritual at the **green** ward circle with salt in hand.
5. Resolve all three houses to win. Lose if health or resolve hits zero.

**Design rule:** bullets stagger monsters and buy time — knowledge (clues + ritual)
resolves curses.

## Controls

| Key | Action |
|---|---|
| WASD / arrows | move (Shift to sprint) |
| Mouse | aim flashlight |
| Left click / Space | shoot (if ammo > 0) |
| E | interact / collect / ritual |
| F | toggle flashlight |
| N | toggle day / night (testing) |
| M | show / hide map |
| 1 / 2 / 3 | choose faction (title screen) |
| R | restart |

## Color language

- **Purple** — interactive curse risk (trigger objects, curse light)
- **Red** — danger: hunts, sealed exits, mimic tells
- **Blue** — clues and evidence
- **Green** — ward circles, ritual success, safety

## Faction passives

- **Celtic (Order of the Black Star):** senses hidden doors and purple curse objects from afar.
- **Assyrian (Star-Priests of the Ledger):** identifies forged clues, slows hunters.
- **Egyptian (House of Duat):** greater resolve pool, faster judgment rituals.

## Systems in the prototype

Village world map with safehouse · house interiors as tile floorplans (4–6 rooms, inner
doors, hidden doors) · full curse state machine · hunter monster with stagger ·
mimic teammates spawned by isolation, revealed by flashlight · survival needs (health,
stamina, resolve, hunger, thirst, battery) · day/night · flashlight cone lighting ·
false clues · clue log · field map (which lies during Distortion) · synthesized WebAudio cues.
