# SamSho Reader

**English** · [Español](README.es.md) · [Deutsch](README.de.md) · [Français](README.fr.md) · [Italiano](README.it.md) ·
[Português (Brasil)](README.pt-BR.md) · [日本語](README.ja.md) · [한국어](README.ko.md) · [简体中文](README.zh-CN.md) · [繁體中文](README.zh-TW.md)

A screen-reader mod for **SAMURAI SHODOWN** (2019; Steam, PC). It speaks the game's menus, story, command lists, tables and on-screen text through the screen reader you already use (NVDA, JAWS), in the language the game is running in.

By Bruno Broiero, with help from Claude.

## What it does

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

Not read:

- The congratulations screen at the end of the story is a picture with no text.
- Online rooms and chat were not tested with opponents.

## Installing

You need the Steam PC version of SAMURAI SHODOWN, Windows x64 and a running screen reader (NVDA or JAWS). UE4SS, the mod loader for Unreal games, comes inside the zip, in the build that works with this game.

Extract everything in the zip into `SamuraiShodown\Binaries\Win64` (in Steam: `steamapps\common\SamuraiShodown\SamuraiShodown\Binaries\Win64`): `dwmapi.dll`, the `ue4ss` folder and these READMEs.

Start the game from Steam, not from the .exe: without Steam it starts in English and offline. The mod says "SamSho Reader" as soon as it is running; if you do not hear it, F8 names the screen reader it found. No game file is modified.

To uninstall, delete `dwmapi.dll` and the `ue4ss` folder. UE4SS and PRISM, the library that speaks to the screen reader, ship under their own licences: see `THIRD-PARTY.md`.

## Keys

Outside a fight:

| Key | Gamepad | What it does |
|---|---|---|
| F1 | Right stick left or right | Says everything held (a command list, a table, a result) |
| F2 / F3 | Right stick up / down | Previous / next piece of what is held |
| F10 | Right stick click | Changes the command notation (Normal, Arcade, Arcade simplified, FGC, FGC simplified). The choice is saved |
| F4 | Right stick click, when nothing is held | Reads the screen's button legend ("9 or A Confirm, 0 or B Back") |

In a fight:

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

Always:

| Key | Gamepad | What it does |
|---|---|---|
| F6 | L3 + R3 (both sticks pressed together) | Turns the mod off and back on, confirmed with the game's words for on and off. Not saved: it always starts on |
| F8 | | Names the screen reader the mod uses |

## What F1, F2, F3 and the right stick read

Many screens show more than what is under the cursor: a command list, a result's scores, a table of records, a lesson. The mod does not read all of that on arrival: it keeps it and hands it over with these keys: F3 moves to the next piece, F2 back to the previous one, and F1 says it all at once. At the end, F3 says nothing: that is how you know there is no more. On a pad, the right stick does the same: down is F3, up is F2, left or right is F1.

What a piece is depends on the screen:

- **Command list**: each move with its input, in the notation chosen with F10 or the stick click; changing it repeats the move in the new one. On entering, the fighter and the category are said.
- **Tutorial**: each sentence of the explanation and of the task, with the inputs put into words; the click changes their notation too.
- **Result**, after a fight: the winner's line is said on its own; the scores wait in the keys, on purpose, so that the line is not buried under figures.
- **Versus result**: wins, losses, draws, rate and points of each side.
- **Player data**: the tables of records and rankings, one row per piece; on arrival the title and the first row are said.
- **Button legend**: with nothing kept, the stick click (or F4) reads the screen's own legend of buttons.

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

## Reporting a problem

Quit the game normally and send `SamuraiShodown\Binaries\Win64\ue4ss\UE4SS.log`: it records what the game displayed and what the mod said about it, in the exact words, so there is no need to write down what you heard. Say which screen it was and what you expected to hear.

## Building

The mod is Lua, loaded by UE4SS; nothing is compiled except `prism_bridge.dll`, the small native module that hands speech to PRISM and reads the pad (`native\prism_bridge\build.ps1`, needs MSVC). `python tools\package.py` builds the release zip from the game folder.

## Translations

This README ships in every language the game supports. Only the English and Spanish ones have been checked by a speaker; corrections to the rest are welcome. The mod itself speaks the game's language: almost everything it says is the game's own text, and its few words of its own (directions, key names, "life", "rage") were checked by ear in Spanish only.
