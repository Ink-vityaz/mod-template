# Making a mod here

Each folder in `mods/` is one mod of Vityaz Hero, data only: no code.

- A folder's name is the mod's id (lower case letters, digits, `_`) and is written the same in `bundle.json`,
  `module.json`, the `modules` or `content` list and the folders inside.
- `bundle.json` lists what is on disk: each folder of `modules/`, each file of `data/`, nothing else.
- `listing.json` is what the mods page shows: `author` (40 letters at most) and `about` (one line, 160 at most). Put the
  author's own words in place of the sample ones.
- Raise `version` in `bundle.json` with every change handed out. Keep `game` to versions the mod was tried on.
- Never set `needs_server`, and use no `button` cell, `op`, `script`, `.gd`, `.cs` or `.dll`.
- The variables a panel may show, every field and every error: https://vityaz.ink.io.vn/mod/llms.txt. Use only what is
  listed there; an unknown variable shows as a dash, an unknown theme name refuses the whole theme.
- Files are UTF-8 JSON without comments. The words a player reads are Vietnamese.
