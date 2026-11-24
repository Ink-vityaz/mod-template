---
name: vityaz-theme
description: Make or change a Vityaz Hero theme mod, the game's colours, text sizes, pictures and backgrounds in one JSON file with no code. Use when the user wants another look ("giao diện", "đổi màu", "theme", a festival look), or mends one the game refuses. Not for windows of numbers (vityaz-panel), nor for handing a mod in (vityaz-share).
---

# A theme

Start from `mods/my_theme`, or from the theme the user names. A theme says only what it changes; the rest stays the game's.

## Read first

Fetch these; what they say stands over this file and over memory. If they cannot be fetched, say so and use only the
names already in this repository.

- https://vityaz.ink.io.vn/mod/themes/index.md: what a theme can change
- https://vityaz.ink.io.vn/mod/reference/fields/index.md: every field and every name of a colour and a size
- https://vityaz.ink.io.vn/mod/reference/errors/index.md: what the game says when it refuses a theme

## Steps

1. Say which colours, sizes and fills answer the wish, by their names on the fields page.
2. For a new mod, copy `mods/my_theme` to `mods/<id>`; never rename the sample. The same new id goes in
   the folder `mods/<id>`, `id` and `content` in `bundle.json`, the file `data/ui/themes/<id>.json` and `id` in it, and
   the file `locale/<id>.csv`. `display_name` and the key in the CSV are
   the same new word, `THEME_<ID>`.
3. Set `name` in `bundle.json`, the theme's name in the CSV, and the mod's `README.md`.
4. Fill in `listing.json`. Ask the user for `author` when it is not known; never make one up.
5. Check: skill `vityaz-share`, "Check".
6. Tell the user how to try it, below. Say it is untried until they have.

## Rules

- One unknown name refuses the whole theme: copy names from the fields page, never guess.
- Colours are `"#rrggbb"` or `"#rrggbbaa"`. Sizes are within the limits the themes page gives.
- Words must stay readable: check `text`, `dim`, `accent` and `danger` against `back`, and `on_accent` against `accent`,
  4.5 to 1 at least for what the theme sets. Where the other colour is the game's and not known, say so.
- No `decor`, `fonts` or shader: mods-community does not take them yet, though the themes page shows them.

## Try it in the game

Hero window, gear, **Mod**, **Nhập thư mục**, choose `mods/<id>`. Open the game again, then Settings, **Giao diện**, and
choose the theme. When the game keeps its own look, its log in `%APPDATA%\VityazHero\logs` has a line with
`the theme <id> is not shown` and the error's code.
