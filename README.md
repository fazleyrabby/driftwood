# Driftwood

A pixel-art island survival game in a single HTML file. You wash ashore on an unknown tropical island. Gather, craft, build a camp, ride out storms, and light a signal fire when a ship passes.

It's all 3D rendered at low resolution with outlines so it reads as pixel art. Built with [Three.js](https://threejs.org) 0.160: no build step, no asset files. The island, art, icons and sound are all generated in code.

## Play

Open `index.html` through any local web server (ES modules don't load from `file://`):

```bash
python3 -m http.server 4351
```

Then visit http://localhost:4351. Three.js loads from jsDelivr and the fonts from Google Fonts, so you need to be online.

## How to play

**The goal:** get rescued. Build a signal fire on the hilltop, then light it while a ship is passing.

The **Survival guide** card (top right) walks you through it one step at a time and ticks each step off. Press **J** to fold it, or turn it off in Settings.

1. **Drink.** Click a palm to shake down coconuts, then right-click the coconut in your hotbar. Coconut shells can be refilled with boiled water at a campfire or from a rain catcher.
2. **Gather.** Click sticks, stones, fiber grass, leaves, driftwood and fruit bushes. The castaway keeps working nearby things of the same kind, like an RTS villager. Clams only come out at low tide.
3. **Craft** (C). Rope from fiber, then a stone knife (stone + flint from the rocky hill), a stone axe, a hammer, a torch and a spear. Cook at any campfire; cut planks at a workbench.
4. **Build** (B). Pick a structure and click the ground; R rotates it. The castaway hammers it up. Structures:
   - **Lean-to:** shelter and faster sleep.
   - **Campfire:** warmth, cooking, rest.
   - **Torch post:** light at night.
   - **Rain catcher:** fresh water.
   - **Storage crate:** keeps items safe even if you die.
   - **Workbench:** a crafting station.
   - **Tent:** needs sailcloth from storm wreckage.
   - **Signal fire.**
5. **Survive.** Watch hunger, thirst, energy, warmth and health (top left).
   - Night is cold, so stay near a fire or sleep in a lean-to.
   - Rain soaks you, which drains warmth faster.
   - Midday sun burns you; wear a sun hat or stay in jungle shade.
   - If you collapse, you wake by the fire, and your things wait in a pouch where you fell.
6. **Weather.** Clouds warn you an hour ahead, and the minimap flashes red before a storm. Storms damage buildings and put out unsheltered fires. Afterwards, driftwood and a supply crate wash ashore.
7. **Food.** At night, crabs come out on the beach; click one to catch it. Hold the spear and click shallow water to fish: strike when the marker is in the gold zone.
8. **Rescue.**
   - Fell palms with the axe (select it in the hotbar, then click a palm) for 4 logs.
   - Dry fronds into thatch at a campfire.
   - Build the **signal fire** on the hilltop.
   - From day 2, ships pass in the evening. When the horn sounds, click the signal fire to light it.

### Controls

| Input | Action |
|---|---|
| Left click | Walk there, or gather / use what you point at |
| Shift + click | Queue orders (also places more buildings) |
| Drag, screen edge | Pan |
| Scroll, + / − | Zoom (up to 3×) |
| Q / E | Turn the view |
| Space | Find the castaway (strike while fishing) |
| WASD / arrows | Walk directly |
| F | Gather the nearest thing |
| 1–8 | Select a hotbar slot (the selected tool is held) |
| Right-click a slot, U | Eat, drink, use |
| Shift + click a slot | Move a stack between hotbar and bag (or crate) |
| I / C / B / O | Bag / Crafting / Build / Settings |
| R | Rotate a building while placing it |
| J | Fold the survival guide |
| H | Hide the HUD |
| P | Save a postcard (PNG of the current view) |
| Esc | Close a panel, cancel placing, stop the current orders |
| F8 / F9 / F10, T, G, F6 | Debug: storm, +1 hour, dawn, time of day, logic grid, reveal fog |

The game saves itself every 30 seconds, at dawn and when you leave the tab. The title screen has **Continue**, **New game** and **New island** (a fresh seed). Settings has pixel size, outlines, color depth, graphics quality, a Relaxed mode (no meters or storm damage) and sound.

## Files

- `index.html`: the whole game.
