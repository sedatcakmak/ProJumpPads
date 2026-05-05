# ProJumpPads

A jump pad plugin for Spigot/Paper. Set up two corner positions to define a pad area, configure a launch destination, attach commands, particles, and sounds, and optionally gate each pad behind a permission.

Originally created by qKing12; continued and maintained by SedatTR.

## Features

- Define jump pads by selecting two block positions (pos1 / pos2) on a configured block type (default: slime block).
- Per-pad teleport / fly destination.
- Per-pad command execution when a player triggers the pad.
- Per-pad permissions and custom permission-denied message.
- Configurable launch power, sounds (launch / flying / land / no-permission) and particles (jump pad / travel / no-permission).
- Optional Multiverse-Core and PlaceholderAPI integration (soft dependencies).
- In-game setup guide and pad info / list commands.

## Requirements

- Minecraft / Spigot 1.16+ (built against Spigot API 1.16.4).
- Java 8 or newer.
- Optional: Multiverse-Core, PlaceholderAPI.

## Commands

- `/jumppads` (alias: `/jumppad`) — base command. Subcommands include:
  - `create [name]`, `delete [name]`
  - `pos1 [name]`, `pos2 [name]` (look at a block to set)
  - `set-fly-location [name]`
  - `add-command [name] [command]`, `remove-command [name] [command]`
  - `set-permission-1 [name] [permission]`, `set-permission-2 [name] [permission]`
  - `set-permission-message [name] [message]`
  - `teleport [name]`, `info [name]`, `list`
  - `guide`, `reload`

The base command permission is `jumppads.command` by default (set to `""` in config to disable).

## Installation

1. Drop `ProJumpPads.jar` into your server's `plugins/` folder.
2. Start (or restart) the server to generate `config.yml`.
3. Edit `plugins/ProJumpPads/config.yml` to taste, then `/jumppads reload`.

## Configuration

`config.yml` controls:

- `settings.push` — launch power and Y velocity.
- `settings.block` — the block type that acts as a pad.
- `settings.permission` — permission for the base command.
- `settings.sounds` and `settings.particles` — per-event sounds and particles.
- `messages` — all in-game messages (color codes supported).

Use `/jumppads guide` in-game for a step-by-step setup walkthrough.
