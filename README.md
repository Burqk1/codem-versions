# CodeM Versions

Current version and changelog records for the scripts. `versionchecker.lua` on
customers' servers reads this repo.

This repo contains no code, only data. Folder names, file names and the format
below are read by scripts on customer servers, so changing them affects every
deployed installation. `versionchecker.lua` is not in this repo; the reading
and comparison logic lives inside each script. The repo's default branch is
`main`.

## Structure

    <script-adi>/
      version.json    guncel surum
      changelog.md    surum notlari

The folder name must match the `VersionChecker.key` value on the script side
exactly. Renaming a folder breaks the version check for customers using that
script.

## Registered scripts

    codem-admin                  codem-motelcreator
    codem-camera                 codem-pettycrimes
    codem-carservice             codem-phone
    codem-clothing               codem-racing
    codem-dispatchv2             codem-radiov2
    codem-dynamicweather         codem-supreme-hud
    codem-emotemenu              codem-supreme-market
    codem-fishing-simulator      codem-supreme-multicharacter
    codem-fuel                   codem-supreme-settings
    codem-gps                    codem-supreme-uipack
    codem-inventoryv2            codem-tv
    codem-mdtv2
    codem-mechanicv2

The current versions are in each folder's `version.json` file.

## Releasing a new version

1. Bump the `version` value in the script's `fxmanifest.lua`
2. Set the `version` value in `<script-adi>/version.json` here to the same value
3. Add a new block at the top of `<script-adi>/changelog.md`

Example commit message: `codem-mdtv2 2.0.9`.

## Adding a new script

Create a new folder and put `version.json` and `changelog.md` in it. On the
script side, set the `VersionChecker.key` value in `versionchecker.lua` to the
same value as the folder name.

## version.json

    {
        "version": "1.4",
        "critical": false,
        "message": ""
    }

- `version`   : required, must match `fxmanifest.lua`
- `critical`  : if true, prints "KRITIK GUNCELLEME" ("CRITICAL UPDATE") in the console
- `message`   : if filled in, shown as a single line above the changelog

Notes:

- Key order doesn't matter (it just has to be valid JSON). In some files
  `critical` and `message` are written first.
- The version format differs from script to script: `codem-phone` uses two
  parts (`3.20`), `codem-inventoryv2` uses three parts (`2.49.0`). Since the
  comparison logic is inside `versionchecker.lua`, don't change a script's
  existing format; always write it the same as in `fxmanifest.lua`.
- Currently no script has `critical: true` or a non-empty `message`.

## changelog.md

    ## 1.4 - 2026-09-10
    - Yeni CCTV kayit sistemi
    - Warrant sure ayari duzeltildi

    ## 1.3 - 2026-09-02
    - Overview istatistik ekrani

- Header: `## <surum> - <tarih>` (version - date; the date is optional)
- Items: lines starting with `- `
- Newest version at the top
- Customers only see versions newer than their own

### "Changed files" section

In most blocks, after the items, there is a `### Changed files` subheading
that lists which files changed:

    ## 1.0.3 - 2026-11-06

    - Fix: TV picture flickering on stock TV models

    ### Changed files

    fxmanifest.lua: version 1.0.3
    config/config.lua: Config.NowPlaying

The lines in this section don't start with `- `, so under the rule above they
are not counted as items. Make sure these lines don't start with `- `. How this
section appears in the customer's console is determined inside
`versionchecker.lua` and can't be verified from here.

## Checklist

Before publishing:

- Does the `version` in `version.json` match the version in the topmost `## `
  header in `changelog.md`?
- Do both match the `version` in the script's `fxmanifest.lua`?
- Is `version.json` valid JSON (no trailing comma, double quotes)?

Things to watch for in the current state:

- `codem-carservice/changelog.md` only has a `## 1.0.1` header and a single
  "Initial release" item; the real notes and date for this version are unknown.
- The `## 1.2` header in `codem-dynamicweather/changelog.md` has no date.
  Since the date is optional, this is within the rules.
