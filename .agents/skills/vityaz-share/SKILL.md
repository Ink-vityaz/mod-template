---
name: vityaz-share
description: Check a Vityaz Hero mod, mend what the check or the game says is wrong, and get it ready to hand in to the community mods. Use before sharing or updating a mod, when a pull request's check is red, or when the Mod window shows an error ("mod không chạy", "kiểm mod", "nộp mod"). Not for making a new mod (vityaz-panel, vityaz-theme).
---

# Check and share

## Check

Go through the list for each mod the user works on, in the files themselves, not from memory. Then run the checker when
Rust and git are here; the user's own repository on GitHub runs it on every push too.

```
git clone https://github.com/Ink-vityaz/mods-community ../mods-community
cargo run --release --locked --manifest-path ../mods-community/tools/mods_community/Cargo.toml -- check --root .
```

Ask before cloning. Without Rust, do not install it: say that the checker was not run and that GitHub will run it.

- The folder's name, `id`, the folders and files inside and the `modules` or `content` list hold one id.
- Every folder of `modules/` and every file of `data/` is listed in `bundle.json`, and the other way round.
- `format` is 1, `version` three numbers, `name` at most 40 letters, `game` a range such as `0.29.x`, never `x`
  (the game reads `x`, mods-community does not take it), `depends` empty.
- `README.md` and `listing.json` are there; `author` at most 40 letters, `about` one line of at most 160.
- No sample words left: "Tên của bạn", "tên của bạn", "Một dòng nói", "Bảng của tôi", "Giao diện của tôi", "Xin chào từ
  mod của bạn!", the ids `my_panel` and `my_theme`. The checker does not look for these.
- Only `json`, `png`, `csv`, `md` and `txt`; 512 KB a file, 2 MB and 100 files a mod, pictures up to 2048 pixels a side.
- JSON with no comment and no comma after the last item; files in UTF-8 without a BOM.
- No code: no `script`, `needs_server`, `op`, `call`, `button` cell, `decor`, `fonts` or shader.

The rules are https://github.com/Ink-vityaz/mods-community; where they differ from this list, they stand.

## Mend

Find the sentence the game or the checker says in https://vityaz.ink.io.vn/mod/troubleshooting/index.md or
https://vityaz.ink.io.vn/mod/reference/errors/index.md, change only what it names, and check again. Never take out a
check, and never change this repository's workflow, to make a red check green.

## Share

1. For an update, `version` is higher than the one handed in before. Skip this for a mod's first time.
2. Ask the user whether they tried this version in the game, on which game version, and whether every picture and word
   is theirs or allowed. Their answers go in the pull request; do not answer for them. The mod's
   own files say nothing of whether it was tried: players read them.
3. They fork https://github.com/Ink-vityaz/mods-community, copy `mods/<id>/` into its `mods/`, loose files and not a
   .zip, and open a pull request. Only files in `mods/<id>/` may change there.
4. Pushing, forking and opening the pull request are the user's: do them only when asked, after listing the mod's files and
   the pull request's words.
