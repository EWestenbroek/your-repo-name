# Carrot Worms — iPhone Game

Status: exploring

## Problem / Motivation

Originally: build an iPhone game in the spirit of the old *Worms* series —
turn-based artillery combat on destructible 2D terrain — themed around
carrots.

That reskin-only version felt too close to being just "Worms with carrots."
The concept has since evolved toward a core loop that's notably different
from Worms while staying 2D and turn-based, with vegetables driving distinct
mechanics rather than just being cosmetic skins on the same weapon-and-aim
formula.

## Rough Approach

**Core loop (combines two earlier directions):**
- No weapons/aiming/projectile physics. Instead, an **underground
  tug-of-war**: vegetables dig/grow toward each other and try to hook onto
  and yank opponents out of the soil to eliminate them. Terrain is tunneled
  through, not blown up.
- Layered with a **shrinking garden bed**: each turn the viable soil shrinks
  (frost line advancing, or a pest working inward), forcing engagements
  instead of letting players stall out digging away from each other
  indefinitely.

**Vegetable roster — each with a distinct verb, not just different stats:**
- **Carrot** — baseline: balanced dig speed and pull strength.
- **Pumpkin** — heavy: very hard to yank out once rooted, but slow to dig
  and a big target once the frost closes in.
- **Bean** — climbs *above* ground via trellis/vines (an escape option
  diggers don't have), and can drop pods that reseed into new bean units
  elsewhere on the board. Turns bean into a multiplying threat: a bean
  player who gets space/time snowballs board presence, but dropped seeds
  can be dug up/destroyed before they take root, and a seed that lands
  where the frost is about to reach is wasted — real timing decisions each
  turn.
- **Potato** — burrows shallow and can go dormant/briefly untargetable, at
  the cost of a wasted turn.
- **Pea** — a pod of several small units instead of one HP pool; picked off
  individually, different risk profile than a single tanky unit.

This gives rock-paper-scissors-ish counterplay (pumpkin walls up but the
shrink eventually catches it; peas spread map presence but die easily; bean
snowballs if left alone but its seeds are a clear counter-target) instead of
every vegetable being an identical reskinned unit.

- Platform: iPhone — likely needs a real 2D engine (SpriteKit, or
  Unity/Godot exporting to iOS) rather than building physics/terrain
  handling from scratch.
- Prototype scope: 2 vegetables (carrot + one contrast, probably pumpkin) to
  prove the tug-of-war-plus-shrinking-bed loop is fun before building the
  full roster.

## Open Questions

- Native (SpriteKit) vs. cross-platform engine (Unity/Godot) — depends on
  whether this ever needs Android too, and comfort with each toolchain.
- Local multiplayer (pass-and-play) only, or online multiplayer eventually?
- Full roster order: which vegetable after carrot + pumpkin proves the loop
  — bean (reseeding) is the most mechanically interesting next, but also the
  most complex to build.
- Balance questions once more vegetables exist: how strong should bean's
  reseeding be before it needs a hard cap (max seeds alive, cooldown, etc.)?
- Naming/branding — no longer just "carrots," so "Carrot Worms" may not fit
  the final concept. Revisit once the roster is more settled.
- Since the core loop now meaningfully diverges from Worms, trademark/
  lookalike concern from the original framing is much less of an issue —
  but worth a final sanity check before any public release either way.

## Links / Resources

- Original reference point: Worms (Team17) series — now more of a genre
  ancestor than a template, since the tug-of-war/shrinking-bed loop and
  vegetable-specific verbs are meant to differentiate from it.
