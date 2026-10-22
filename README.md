# SamSho Reader

**English** · [Español](README.es.md) · [Português (Brasil)](README.pt-BR.md) · [Français](README.fr.md) ·
[Italiano](README.it.md) · [Deutsch](README.de.md) · [日本語](README.ja.md) · [한국어](README.ko.md) ·
[简体中文](README.zh-CN.md) · [繁體中文](README.zh-TW.md)

An accessibility mod for **SAMURAI SHODOWN** (2019, Steam): it makes the game readable with your screen reader. Menus, options, character and stage select, story subtitles, the tutorial, the command list, the database, the gallery, online, results and the fight's own numbers.

Almost every word you will hear is the game's own, in the language the game is set to. The few words the game has none for (command directions, key names, "life", "rage") are translated into the game's eleven languages.

Author: **Bruno Broiero**. Built with Claude.

## Requirements

- SAMURAI SHODOWN for Steam (Windows).
- A running screen reader: NVDA or JAWS. The mod speaks through PRISM.
- [UE4SS](https://github.com/UE4SS-RE/RE-UE4SS), the mod loader for Unreal games. It comes inside the download, in the build that works with this game (experimental, 21 September 2026): there is nothing to fetch separately.
- An XInput (Xbox-style) gamepad is optional, but the mod is designed around one.

## Installation

1. Download the latest `SamShoReader-x.y.z.zip` from [Releases](../../releases).
2. Extract everything in it into `SamuraiShodown\Binaries\Win64\` (the game folder; in Steam: `steamapps\common\SamuraiShodown\SamuraiShodown\Binaries\Win64`): `dwmapi.dll`, the `ue4ss` folder and the READMEs.
3. Launch the game **from Steam** (not from the .exe: without Steam it starts in English and offline).
4. When it loads, the mod says "SamSho Reader". If you do not hear it, press F8: it names the screen reader it found.

## The mod's keys

| Key | Gamepad | What it does |
|---|---|---|
| F1 | Right stick left or right | Says everything held (a command list, a table, a result) |
| F2 / F3 | Right stick up / down | Previous / next piece of what is held |
| F10 | Right stick click | Changes the command notation (Normal, Arcade, Arcade simplified, FGC, FGC simplified). The choice is saved |
| F4 | Right stick click, when nothing is held | Reads the screen's button legend ("9 or A Confirm, 0 or B Back") |
| F7 | | Stops the voice |
| F6 | L3 + R3 (both sticks pressed together) | Turns the mod off and back on, confirmed with the game's words for on and off. Not saved: it always starts on |
| F8 | | Names the screen reader the mod uses |
| Ctrl + Escape | | Silences speech |

The arrows, Enter and Backspace belong to the game, not the mod.

## In the fight

Nothing speaks by itself: the fight can already be heard. The right stick asks for the figure you need:

| Right stick | Says |
|---|---|
| Left | Both sides' life: "life 71%, 80%" (your side first) |
| Up | Rage: "rage 41%, max" |
| Down | Rounds won: "ROUNDS 1, 0". In Survival, Time Trial and Ironman, your wins in a row |
| Right | The round's clock |
| Click | All of it |

Keyboard: F2 life, F3 rage, F10 rounds, F1 all.

In Survival, Time Trial and Ironman only your own side is given.

## The command list and its notations

In the game a command is a row of pictures: arrows, buttons, a "plus", conditions. The mod turns them into words, and since players come to a command list from different places (the arcade, the forums, or neither), it offers five ways of saying them. F10 or the right stick's click changes it, and the choice is saved. The same command, quarter circle forward and heavy slash, in each:

| Notation | How it sounds |
|---|---|
| Normal | down, diagonal down forward, forward plus Heavy Slash |
| Arcade | quarter circle forward, Heavy Slash |
| Arcade simplified | quarter circle forward, C |
| FGC | 2 3 6, Heavy Slash |
| FGC simplified | 2 3 6, C |

- **Normal** says every direction with its word. The longest, and the one that assumes nothing.
- **Arcade** names the shape: quarter circle, half circle, dragon punch and their reverses. The way commands are said out loud.
- **FGC** uses the numpad digits, the community's notation: 6 is forward, 2 down, 3 the down-forward diagonal; always facing right.
- The **simplified** variants replace the buttons' names with the cabinet's letters: A light slash, B medium, C heavy, D kick.

How the reading was designed, because a picture says things with its shape that words have to say out loud:

- A diagonal is one input, so it is called "diagonal": "down, diagonal down forward, forward". Said as "down, down forward, forward" nobody can tell two inputs from one.
- Two buttons drawn touching are pressed together, so they are joined with "plus" in every notation.
- A condition the game draws around the move's name ("during ~") is said once, not as two halves.
- A condition like "repeatedly" is said after the buttons it applies to: "forward plus Light Slash, repeatedly" - how it is said, not how it is drawn.
- The buttons' and conditions' names are the game's words, taken from the legend of its own command list; directions, shapes, "plus" and "or" are the mod's, in the eleven languages.
- "Or" comes several ways in the game (two alternative buttons, two commands, a list); all are said with the same word.

The list is walked with the right stick (up and down, move by move; left or right, whole) or with F2, F3 and F1. On entering it says the fighter and the category ("SHIKI, SPECIAL MOVES"), then each move as "name, condition if any: command", for example "Elysium Halo: forward, down, diagonal down forward plus Light Slash or Medium Slash or Heavy Slash".

## What is read

- The main menu and every submenu, with each entry's description.
- Options: game, display, sound (volumes in %), language and subtitles, button config (each action with its key or button).
- Character select, including random, costumes and colours; stage select; side assignment in Versus.
- Story: subtitles and dialogue, unlocks, epilogue and credits.
- Tutorial: instruction, task and closing message, with the keys as words.
- Command list: every move with its command in the notation you choose; walked with the stick or F2 / F3.
- Pause and Training settings.
- Database: profile, own rankings, general records.
- Gallery: movies, artwork, voices and music, with their tabs and pages.
- Online: leaderboards, ranked and casual battle screens, ghost lists in Ghost Battle.
- Results: the winner's line is read by itself; the score is held and asked for with the stick or F1.
- Unlock banners and notices.

## What is not read

- The congratulations screen at the end of the story is a picture with no text.
- Online rooms and chat were not tested with opponents.

## Languages

The mod speaks the game's language. The mod's own words were checked by ear in Spanish only; in the other languages they are translated without a speaker having reviewed them. A wrong word is a bug worth reporting.

## Notes

- The mod changes no game file.
- UE4SS is by the RE-UE4SS team, under the MIT licence; `prism.dll` and `tolk.dll` come from [PRISM](https://github.com/ethindp/prism), under the MPL 2.0. See `THIRD-PARTY.md`.
- To uninstall, delete `dwmapi.dll` and the `ue4ss` folder.
- The mod's source is not public yet; it will be once the mod has settled into use. The download is free to use.
