# Third-party files shipped with SamSho Reader

The download carries files the mod did not write. They come from two projects, and both are
shipped unmodified.

## UE4SS

| File | Project | Licence |
|------|---------|---------|
| `dwmapi.dll` | [UE4SS](https://github.com/UE4SS-RE/RE-UE4SS) by the RE-UE4SS team — the proxy that loads it | MIT |
| `ue4ss\UE4SS.dll` | UE4SS itself, the mod loader for Unreal Engine games | MIT |
| `ue4ss\UE4SS-settings.ini` | UE4SS's settings file, with the values this game runs with | MIT |
| `ue4ss\UE4SS_SDK_Backends\UE4SS.json` | part of the UE4SS release | MIT |
| `ue4ss\Mods\shared\UEHelpers\UEHelpers.lua` | UE4SS's Lua helper library, which the mod uses | MIT |
| `ue4ss\Mods\Keybinds\Scripts\main.lua` | UE4SS's built-in keybinds mod, which UE4SS expects to find | MIT |
| `ue4ss\LICENSE` | the MIT licence text of UE4SS | — |

The build shipped is UE4SS's **experimental** line as of 21 September 2026 (v3.0.1-1140).
The stable release of April 2024 cannot be used instead: on this game it crashes at boot.

- Source and licence: <https://github.com/UE4SS-RE/RE-UE4SS>
- Licence text: <https://opensource.org/licenses/MIT>

## PRISM

| File | Project | Licence |
|------|---------|---------|
| `ue4ss\Mods\SamShoReader\Scripts\prism.dll` | [PRISM](https://github.com/ethindp/prism) by Ethin Probst | Mozilla Public License 2.0 |
| `ue4ss\Mods\SamShoReader\Scripts\tolk.dll` | PRISM's Tolk-compatible backend, from the same release | Mozilla Public License 2.0 |

`tolk.dll` here is **not** Davy Kager's Tolk library: it is the compatibility backend built
and shipped by PRISM, which is why it falls under PRISM's licence.

Under the Mozilla Public License 2.0, the source of those two files must be available to
anyone who receives them. It is, unmodified, in PRISM's own repository and its releases:

- Source and licence: <https://github.com/ethindp/prism>
- Licence text: <https://www.mozilla.org/MPL/2.0/>

### PRISM's own notice

PRISM uses code from other projects. Reproduced from its `NOTICE` file:

> This project is licensed under the Mozilla Public License version 2.0. Full details are
> available in the LICENSE file.
>
> This project uses code from other projects. Specifically:
>
> * The `simdutf` library is licensed under the Apache-2.0 license, and is used for Unicode
>   validation and conversion.
> * On Windows, Prism includes NVDA controller client RPC definitions originally under
>   LGPL-2.1 (and generated RPC stubs from those inputs). The Prism project has received
>   permission to license the IDL files (and there generated outputs) under the MPL-2.0
>   regardless of the original license. Thus, you may assume that they are licensed under
>   the MPL-2.0. The LGPL headers and license file in the LICENSES directory remain for
>   providing attribution.
> * On Windows, Prism uses Moderncom by Alexander Bessonov. That code has been maintained
>   by Prism since it's integration, but that code remains licensed under the MIT License,
>   as was the original project.
> * Prism uses dr_libs (specifically, dr_wav) by David Reid for PCM sample handling and
>   conversion (among other things) in `prism_backend_speak_to_memory`. Per the software's
>   license, Prism has opted to license the library under the public domain.
> * Prism uses Djinni, and it's associated support library, originally by Dropbox but forked
>   by Snapchat, for JNI communication and interoperability on Android. The support library,
>   under `third_party/djinni`, is licensed under the Apache License, version 2.0. The
>   auto-generated code, under `source/backends/android`, is under Prism's license.
> * Prism uses `concurrentqueue` by Cameron Desrochers. Prism has opted for the simplified
>   BSD license for this library.
> * Prism uses the `{fmt}` library, by Victor Zverovich and `{fmt}` contributors, for string
>   formatting and the like. That code is licensed under the MIT license.
>
> All licenses may be found under the LICENSES directory.

## The mod itself

Everything else under `ue4ss\Mods\SamShoReader\` — the Lua scripts and `prism_bridge.dll`,
the small native module that hands speech to PRISM and reads the gamepad — is SamSho Reader,
by Bruno Broiero. Its source is not public yet (see the README); the download is free to
use and share as it is.

SAMURAI SHODOWN is the property of SNK Corporation. This mod is an unofficial, unaffiliated
accessibility tool: it ships no part of the game and modifies no game file.
