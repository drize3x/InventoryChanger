# cs2-inventory-changer

Client-side inventory and skin changer for Counter-Strike 2.

[![License](https://img.shields.io/github/license/USER/REPO)](LICENSE)
[![Release](https://img.shields.io/github/v/release/USER/REPO)](https://github.com/USER/REPO/releases)
[![Build](https://img.shields.io/github/actions/workflow/status/USER/REPO/build.yml)](https://github.com/USER/REPO/actions)

Changes how items appear in your own game client. Nothing is sent to Valve, nothing is added to your Steam account, and other players do not see the changes.

> [!WARNING]
> This tool modifies the game client. Using it may result in a VAC ban or other action against your account. Do not use it on VAC-secured servers or on an account you care about. See [Disclaimer](#disclaimer).

## Features

- Skins for weapons, knives and gloves, including wear, pattern seed and StatTrak
- Agents, music kits, pins and coins
- Config profiles that can be saved, loaded and exported
- [feature]

## Requirements

- Windows 10 or 11, x64
- CS2, launched with `-insecure`
- [runtime, e.g. Visual C++ Redistributable 2022]

## Installation

1. Download the latest build from [Releases](https://github.com/USER/REPO/releases).
2. Extract the archive.
3. Launch CS2 with `-insecure`.
4. Run `[executable]`.

## Usage

| Key      | Action               |
| -------- | -------------------- |
| `Insert` | Open / close menu    |
| `[key]`  | [action]             |

Configs are stored in `%APPDATA%\[folder]\configs`.

## Building from source

Requires Visual Studio 2022 with the *Desktop development with C++* workload.

```bash
git clone https://github.com/USER/REPO.git
cd REPO
cmake -B build -A x64
cmake --build build --config Release
```

Output: `build/Release/[name].dll`

## How it works

[2-4 sentences: how the changer finds and replaces item data in memory, what it hooks, how it stays client-side. Skip this section if you'd rather not document internals.]

## Known issues

- Game updates can break offsets until the next release.
- Changes are visible only to you and reset on restart unless a config is loaded.

## Contributing

Issues and pull requests are welcome. For larger changes, open an issue first so we can agree on the approach.

## Disclaimer

This project is not affiliated with or endorsed by Valve Corporation. Counter-Strike and Steam are trademarks of Valve Corporation. The software is provided as is, without warranty. You are responsible for how you use it, including any account penalties.

## License

[MIT](LICENSE)
