# Changer base Neverlose Cr4ck source

In-game overlay menu with a client-side inventory and skin changer for Counter-Strike 2.

Changes apply to your own game client only. Nothing is sent to Valve and nothing is added to your Steam account.

> [!WARNING]
> This project modifies the game client. Using it can result in a VAC ban or other action against your account. Do not use it on VAC-secured servers or on an account you care about. See [Disclaimer](#disclaimer).

This repository is source only. There are no prebuilt binaries, so you build it yourself.

## Features

- Inventory and skin changer: [weapons, knives, gloves, agents, ...]
- Item preview
- Watermark HUD and spectator list
- Configurable keybinds with context-aware handling
- Custom hitsounds and font rendering via FreeType
- Config profiles

## Requirements

- Windows 10 or 11, x64
- Visual Studio 2022 with the **Desktop development with C++** workload
- A Direct3D-capable GPU [adjust if you use another backend]

## Building

```bash
git clone https://github.com/USER/OverlayMenu.git
```

1. Open `OverlayMenu.sln` in Visual Studio.
2. Select the `Release | x64` configuration.
3. Build the solution (`Ctrl+Shift+B`).

Dependencies are vendored under `third_party/`, so nothing needs to be installed separately.

Output goes to `build/x64/`.

## Configuration

Settings are read from `OverlayMenu.ini`. Profiles and assets live in `assets/`.

| Key      | Action            |
| -------- | ----------------- |
| `Insert` | Open / close menu |
| `[key]`  | [action]          |

## Project layout

```
assets/        fonts, hitsounds, logos, profile data
shaders/       HLSL shaders (menu_material.hlsl) and originals
src/
  core/        [short description]
  inventory/   inventory and skin changer logic
  platform/    [short description]
  preview/     item preview
  render/      rendering
  ui/          menu and HUD
tests/         standalone C++ tests and parity notes
third_party/   FreeType, MinHook
```

## Tests

Tests are plain C++ files under `tests/`, one per area (item color, keybind context, native signatures, spectators, watermark HUD, UI dump parity, frost environment). [How to run them, e.g. a separate project or build configuration.]

## Known issues

- Game updates can break signatures until they are updated.
- [other limitations]

## Contributing

Issues and pull requests are welcome. For larger changes, open an issue first so we can agree on the approach. Code style is defined in `.clang-format`.

## Disclaimer

This project is not affiliated with or endorsed by Valve Corporation. Counter-Strike and Steam are trademarks of Valve Corporation. The software is provided as is, without warranty. You are responsible for how you use it, including any account penalties.

## Third-party

- [FreeType](https://freetype.org)
- [MinHook](https://github.com/TsudaKageyu/minhook)

## License

[MIT](LICENSE)
