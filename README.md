# Karabiner-Elements configuration

Personal macOS keyboard configuration, shared as a backup and as a starting point for others. It is tailored to my setup; review and adapt it before using it on another Mac.

## What's here

- `karabiner.json` — complete Karabiner-Elements configuration with two profiles. **`ps` is selected by default**; `Default profile` is retained as an alternate.
- `assets/complex_modifications/` — standalone complex-modification rule exports that can be imported individually in Karabiner-Elements.

The selected `ps` profile includes a SteelSeries Apex Pro TKL modifier swap; Caps Lock and SpaceFN layers; Vim-style navigation; app/tab switching; delete-key remaps; a tmux leader mapping; and Control+/ for menu-bar command search.

The shortcut that used to launch an Orion Page Tweaks script (Ctrl+= / Ctrl+Shift+=) is not present. The machine-specific Kitty launcher rule was also left out of the shared config because it depended on a local script and an absolute home-directory path.

## Install / restore

1. Install [Karabiner-Elements](https://karabiner-elements.pqrs.org/) on macOS.
2. Back up your existing configuration first.
3. Copy `karabiner.json` to `~/.config/karabiner/karabiner.json`, or use Karabiner-Elements' profile/import tools to adapt the rules rather than replacing your whole config.
4. In Karabiner-Elements, confirm the `ps` profile is selected. Reconnect or re-identify your keyboard if device-specific mappings do not apply.
5. Review and import any desired rule from `assets/complex_modifications/` individually.

This is a full configuration, not a universal installer. Replacing your config can overwrite your own profiles and device settings. Keep a backup and inspect the file before applying it.

## Device-specific notes

- The `ps` profile's modifier swap is conditioned on the SteelSeries Apex Pro TKL's vendor/product identifiers. Change those identifiers for a different keyboard, or remove that condition if you want the mapping on every keyboard.
- The profile includes device identifiers and settings that reflect my hardware. They are not credentials, but may need adjustment on another machine.
- Some optional rule exports use Karabiner `shell_command` actions (for example, notifications or resetting SpaceFN state). Inspect those actions before importing rules you do not recognize.

## Privacy / secrets

No API keys, passwords, authentication tokens, or private keys are needed by this configuration. Backups, automatic backups, and local helper scripts are intentionally not included. Please continue to keep secrets and personal machine backups out of commits.
