# Custom Spells — Overview

Documentation for [`mod-custom-spells`](https://github.com/Shoro2/mod-custom-spells).

This folder is the curated, discovery-friendly view of the custom spell system. The single source of truth for the full ID catalog remains [`CustomSpells.md`](https://github.com/Shoro2/mod-custom-spells/blob/master/CustomSpells.md) in the mod repo.

## Base docs

| File | Contents |
|-------|--------|
| [01-architecture.md](01-architecture.md) | repo layout, hooks, loader, build/install |
| [02-id-blocks.md](02-id-blocks.md) | 900xxx ID scheme + allocation table for all specs |
| [03-procs-and-flags.md](03-procs-and-flags.md) | `spell_proc` setup, ProcFlags, SpellFamilyFlags verification, off-by-one BasePoints |
| [04-adding-a-spell.md](04-adding-a-spell.md) | step-by-step recipe for new custom spells |
| [05-complex-spells.md](05-complex-spells.md) | cross-cutting topics: recursion, target caps, ICDs, custom NPCs, owner→pet, OnRemove detection, channel/cast, client patches |

## Spec catalogs

### Warrior (900100–900199)
- [Arms](warrior-arms.md) · [Fury](warrior-fury.md) · [Protection](warrior-protection.md)

### Paladin (900200–900299)
- [Holy](paladin-holy.md) · [Protection](paladin-protection.md) · [Retribution](paladin-retribution.md)

### Death Knight (900300–900399)
- [Blood](death-knight-blood.md) · [Frost](death-knight-frost.md) · [Unholy](death-knight-unholy.md)

### Shaman (900400–900499)
- [Elemental](shaman-elemental.md) · [Enhancement](shaman-enhancement.md) · [Restoration](shaman-restoration.md)

### Hunter (900500–900599)
- [Shared](hunter-shared.md) · [Beast Mastery](hunter-beast-mastery.md) · [Marksmanship](hunter-marksmanship.md) · [Survival](hunter-survival.md)

### Rogue (900600–900699)
- [Assassination](rogue-assassination.md) · [Combat](rogue-combat.md) · [Subtlety](rogue-subtlety.md)

### Mage (900700–900799)
- [Shared](mage-shared.md) · [Arcane](mage-arcane.md) · [Fire](mage-fire.md) · [Frost](mage-frost.md)

### Warlock (900800–900899)
- [Affliction](warlock-affliction.md) · [Demonology](warlock-demonology.md) · [Destruction](warlock-destruction.md)

### Priest (900900–900999)
- [Discipline](priest-discipline.md) · [Holy](priest-holy.md) · [Shadow](priest-shadow.md)

### Druid (901000–901099)
- [Balance](druid-balance.md) · [Feral Tank](druid-feral-tank.md) · [Feral DPS](druid-feral-dps.md) · [Restoration](druid-restoration.md)

### Global / Non-Class (901100–901199)
- [global.md](global.md)

## Conventions

- **One file per spec.** Class-level files do not exist by design — specs evolve independently.
- **Kebab-case file names**, no number prefixes in `specs/` (order is irrelevant, avoid renames).
- **Status markers** per spell: `Live`, `WIP`, `TODO`.
- **Implementation notes** only for non-trivial spells (procs, formulas, edge cases). Trivial entries stay in the table.
- **Architecturally tricky spells** are collected in [`05-complex-spells.md`](05-complex-spells.md) — recurring patterns (recursion guard, target caps, ICDs, custom NPCs, etc.) live there centrally.
