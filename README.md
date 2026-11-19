# Dragon Quest IV, V and VI (Android): French patch

`DQ_Patch_FR.exe` is a Windows tool that translates the Android (Google Play) versions of Dragon Quest IV, V and VI into French.

It reads the official French text from the European DS ROM of each game. Texts that only exist in the mobile versions are translated by the patch. The patched game is then installed on the phone over USB.

The tool's interface is available in English, French, German, Spanish, Italian, Japanese, Chinese and Korean. In English, Japanese, Korean and Chinese, languages that the mobile games already contain, the tool only copies the original APKs and the saves from the phone (for example to use them with a PC port); the French patch is available with the French interface.

## Contents

| Item | Purpose |
|---|---|
| `DQ_Patch_FR.exe` | The tool |
| `THIRD_PARTY_NOTICES.md` | Third-party components and their licenses |
| `roms/` | Folder for your DS ROMs (`.nds`, or a `.zip` containing them) |
| `dependencies/` | Filled by the tool: the installed tool, settings, log and downloaded programs |
| `games/DQ4/`, `games/DQ5/`, `games/DQ6/` | Filled by the tool, one folder per game: `apks`, `texts`, `build`, `patched_apks`, `title_screen`, `signed`, `saves` |

Empty folders only contain a `.gitkeep` file, which keeps them in the repository.

## Requirements

- The game (IV, V or VI), installed from the Google Play Store on an Android phone.
- The European DS ROM of the same game, dumped from your own cartridge:

| Game | European DS ROM | Code |
|---|---|---|
| Dragon Quest IV | Dragon Quest: The Chapters of the Chosen | NTR-YIVP-EUR |
| Dragon Quest V | Dragon Quest: The Hand of the Heavenly Bride | NTR-YV5P-EUR |
| Dragon Quest VI | Dragon Quest VI: Realms of Reverie | NTR-YVIP-EUR |

- A PC running Windows 10 or 11, with about 3 GB of free space.
- A USB cable that transfers data, and USB debugging enabled on the phone.
- An Internet connection on first launch, to download the required programs (adb, portable Java, uber-apk-signer). Nothing is installed in Windows.

## Usage

1. Download the repository (**Code** button, then **Download ZIP**) and extract it to a folder of your own, not inside "Program Files".
2. Copy your DS ROMs into `roms`.
3. Run `DQ_Patch_FR.exe`. On first launch it installs itself into `dependencies`, then offers to download any missing programs.
4. The `roms` folder is used by default; another folder can be chosen with "Choose the ROM folder…".
5. Follow the steps in the game's tab: 1 (copy the game from the phone), 2 (prepare the texts), 3 (patch), 4 (install).

Each step, the options and troubleshooting are described in the tool's Help menu.

## Updating

Close the tool, replace `DQ_Patch_FR.exe` with the new version in the same folder, then run it again. Settings, downloaded programs and the `games` folder are kept (folders of older versions are renamed automatically).

## What the tool does not contain

The tool contains no ROM, no game file and no official text: everything is read on your computer, from your ROM and your game. Do not share your ROMs, the generated APKs or the text file created by the tool.

## Legal

Unofficial project, not affiliated with Square Enix, Armor Project, Bird Studio, ArtePiazza, Nintendo or Google. DRAGON QUEST is a trademark of Square Enix.

The tool is provided as is, without warranty, for personal use with games and cartridges you legally own.

Programs downloaded by the tool, each under its own license: SDK Platform-Tools (Google), Java Temurin (Eclipse Adoptium), uber-apk-signer (Apache 2.0 license). The components included in the exe and all the licenses are listed in `THIRD_PARTY_NOTICES.md`.
