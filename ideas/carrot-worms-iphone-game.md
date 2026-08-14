# Carrot Worms — iPhone Game

Status: idea

## Problem / Motivation

Fancy building an iPhone game in the spirit of the old *Worms* series —
turn-based artillery combat on destructible 2D terrain — but themed around
carrots instead of worms/weapons-grade sheep.

## Rough Approach

- Core loop: same as Worms — turn-based, teams of characters (carrots) on
  destructible terrain, wind/gravity affecting projectiles, last team
  standing wins.
- Theming pass on top of the mechanic: carrots instead of worms, garden/soil
  battlegrounds instead of generic islands, weapon set reskinned around a
  garden/vegetable theme (e.g. watering-can airstrike, compost grenade,
  giant zucchini instead of a bazooka/holy hand grenade).
- Platform: iPhone — likely needs a real 2D engine (SpriteKit, or
  Unity/Godot exporting to iOS) rather than building physics/destructible
  terrain from scratch.
- Destructible terrain + projectile physics is the technically hard part;
  everything else (turn order, UI, theming) is comparatively easy.

## Open Questions

- Native (SpriteKit) vs. cross-platform engine (Unity/Godot) — depends on
  whether this ever needs Android too, and comfort with each toolchain.
- Local multiplayer (pass-and-play) only, or online multiplayer eventually?
- How closely to lean into "Worms but carrots" vs. develop distinct
  mechanics once the core loop is proven — trademark/lookalike concerns if
  ever released publicly under a similar name/branding.
- Scope for a first playable prototype: single weapon, one terrain, 2
  players, no menus.

## Links / Resources

- Reference: Worms (Team17) series for core mechanic.
