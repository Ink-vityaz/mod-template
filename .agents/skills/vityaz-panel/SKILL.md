---
name: vityaz-panel
description: Make or change a Vityaz Hero panel mod, a window of the game's numbers described in panel.json with no code. Use when the user wants a panel, a counter, a tracker, a bar or a list of the game's values ("bảng số liệu", "hiện vàng"), or mends one. Not for colours and looks (vityaz-theme), nor for handing a mod in (vityaz-share).
---

# A panel

Start from `mods/my_panel`, or from the panel the user names. A panel only shows; it changes nothing in the game.

## Read first

Fetch these; what they say stands over this file and over memory. If they cannot be fetched, say so and use only the
fields and variables already in this repository.

- https://vityaz.ink.io.vn/mod/panels/index.md: the kinds of cells
- https://vityaz.ink.io.vn/mod/reference/fields/index.md: every field
- https://vityaz.ink.io.vn/mod/reference/variables/index.md: every variable a panel may show

## Steps

1. Say which variables answer the wish. One with no variable cannot be shown: tell the user, do not invent a name
   or put a near one in its place.
2. For a new mod, copy `mods/my_panel` to `mods/<id>`; never rename the sample. The same new id goes in
   the folder `mods/<id>`, the folder `modules/<id>`, `id` in `bundle.json`, `id` in `module.json` and `modules` in
   `bundle.json`.
3. Set `name` in `bundle.json`, `title` and `cells` in `panel.json`, and the mod's `README.md`.
4. Fill in `listing.json`. Ask the user for `author` when it is not known; never make one up.
5. Check: skill `vityaz-share`, "Check".
6. Tell the user how to try it, below. Say it is untried until they have.

## Rules

- Cells are `value`, `bar`, `list`, `text` or `icon`. Never `button`: it sends a command, which is not taken.
- `bind` and `max_bind` are names of the variables page, written the same. `hero.<i>.level` takes a number for `<i>`.
- The words a player reads are Vietnamese, short enough for the width in `size`.
- A picture is a PNG beside `panel.json`, the user's own or one they may use, its source in `README.md`.
- No `script`, `needs_server`, `op` or `call`, no `.gd`, `.cs` or `.dll`.

## Try it in the game

Hero window, gear, **Mod**, **Nhập thư mục**, choose `mods/<id>`. The round button on the mods' bar opens the panel. The
game runs its own copy, so a later change here must be imported again, with a higher `version`. A cell showing `—` has a
variable the game does not know, or one that is empty now.
