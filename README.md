# AGOT Personal Edits

A personal submod for the [A Game of Thrones](https://steamcommunity.com/sharedfiles/filedetails/?id=2962333032) total conversion mod for Crusader Kings III. It loads after AGOT, so anything here overrides the base mod.

## How overriding works

- **Whole-file override:** put a file at the same relative path and name as the one in AGOT (e.g. `history/characters/stark.txt`), and the game uses yours instead of AGOT's.
- **Add new content:** use a new file name (e.g. `common/traits/zz_my_traits.txt`) and it is loaded alongside AGOT's.
- **Localization:** files in `localization/english/` must end in `_l_english.yml` and be saved as UTF-8 **with BOM**.

Changes to starting history only apply to new games.

## Setup

The game finds this mod through `Documents/Paradox Interactive/Crusader Kings III/mod/agot_personal.mod`, which points at this folder. Edits here are live on the next game launch.

Base mod files for reference: `Documents/Paradox Interactive/Crusader Kings III/mod/AGOT/`.

## Debugging

Errors from your edits show up in `Documents/Paradox Interactive/Crusader Kings III/logs/error.log`.