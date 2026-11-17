# AGOT Realm Overhaul

A game-wide overhaul submod (diplomacy, AI behaviour, balance and other core systems) for the [A Game of Thrones](https://steamcommunity.com/sharedfiles/filedetails/?id=2962333032) total conversion mod for Crusader Kings III. It loads after AGOT, so anything here overrides the base mod.

## How overriding works

- **Whole-file override:** put a file at the same relative path and name as the one in AGOT (e.g. `history/characters/stark.txt`), and the game uses yours instead of AGOT's.
- **Add new content:** use a new file name (e.g. `common/traits/zz_my_traits.txt`) and it is loaded alongside AGOT's.
- **Localization:** files in `localization/english/` must end in `_l_english.yml` and be saved as UTF-8 **with BOM**.

Changes to starting history only apply to new games.

## Setup

The game finds this mod through `Documents/Paradox Interactive/Crusader Kings III/mod/agot_realm_overhaul.mod`, which points at this folder. Edits here are live on the next game launch.

Base mod files for reference: `Documents/Paradox Interactive/Crusader Kings III/mod/AGOT/`.

## Debugging

Errors from your edits show up in `Documents/Paradox Interactive/Crusader Kings III/logs/error.log`.
## Fixes

- **Broken culture repair:** some characters can end up pointing at a deleted culture, which floods `error.log` with `has_cultural_era_or_later ... Culture - 4294967295` and can crash the game. Every quarter the player's pulse finds those characters and gives them a valid culture (father, mother, current location, then liege). To run it immediately in debug mode, open the console and enter `effect agot_ro_repair_broken_cultures_effect = yes`.
