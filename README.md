# VOIDSTRIKE

A 2D open-world space shooter that runs entirely in your browser. No build step, no installs.

**Play it:** open `index.html` in any browser, or visit the GitHub Pages link once Pages is enabled on this repo.

## Controls

| Input | Action |
| --- | --- |
| `W` `A` `S` `D` / arrows | Thrust (forward, reverse, strafe) — relative to where the ship points |
| Mouse | Aim — the ship turns toward your cursor |
| Left click / `Space` | Fire |
| `Shift` | Boost (drains the boost meter) |
| `P` | Pause |
| `M` | Mute |
| `R` | Restart after game over |

## Physics

The game runs on simple Newtonian mechanics:

- **Inertia** — thrust changes velocity, not position. Let go of the keys and you drift.
- **Recoil** — every shot pushes your ship backward.
- **Mass-based elastic collisions** — asteroids bounce off each other and off you; big rocks hit harder because mass scales with radius.
- **Knockback** — bullets transfer momentum to whatever they hit.
- **Splitting** — big meteors break into smaller ones that inherit the parent's velocity plus a kick.

## World

A bounded 22,000 x 22,000 world with a parallax starfield, nebulae, drifting asteroid fields, and enemy ships with seek-and-orbit steering AI. Elites (red, tougher, faster-firing) show up as your score climbs. The minimap in the corner shows the whole world: you (blue), asteroids (grey), enemies (orange).

Destroyed enemies sometimes drop a green hull pickup.

## Files

- `index.html` — the entire game (HTML + CSS + JS, no dependencies)
- `assets1.js` / `assets2.js` — the sprite art, embedded as base64 so the game works served from anywhere
- `LICENSE-assets.txt` — license for the art

Sprites are from Kenney's *Space Shooter Redux*, licensed CC0.

## Credits

Art: [Kenney](https://kenney.nl) (CC0). Everything else: built with vanilla JS and the Canvas API.
