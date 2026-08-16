# macOS US International without dead keys — ISO

A fork of [dnnspaul/macos-us-intl-no-dead-keys](https://github.com/dnnspaul/macos-us-intl-no-dead-keys) with adjusted mappings for ISO keyboards.

This fork is based on the current 2025 version of the upstream layout and keeps its updated US International / AltGr mappings.

## Why this fork exists

The upstream layout already distinguishes between the two relevant macOS keycodes, but assigns the grave/tilde and backslash/pipe pairs in the opposite way from the ISO mapping targeted by this fork.

Upstream:

| Key | Normal | Shift |
|---|---|---|
| ISO extra key | `` ` `` | `~` |
| grave/tilde key | `\` | `|` |

This fork:

| Key | Normal | Shift |
|---|---|---|
| ISO extra key | `\` | `|` |
| grave/tilde key | `` ` `` | `~` |

The same distinction is applied consistently across the relevant modifier maps.

## Changes

Compared with the current upstream layout, this fork:

- maps the ISO extra key to `\` and `|`
- maps the grave/tilde key to `` ` `` and `~`
- applies the corresponding mappings to Caps Lock, Option, Shift+Option, Option+Command, Control, and Command layers
- removes one remaining reachable grave dead-key action from the alternate hardware map
- otherwise preserves the current upstream layout, including its AltGr character mappings and action/state definitions

The `.keylayout` differs from upstream in 16 targeted mappings.

## AltGr characters

The upstream AltGr mappings are preserved.

Examples:

| Shortcut | Output |
|---|---|
| Option+A | `á` |
| Option+E | `é` |
| Option+I | `í` |
| Option+O | `ó` |
| Option+U | `ú` |
| Option+N | `ñ` |

## Installation

Download or clone this repository.

Copy:

```text
US Intl PC without dead keys.bundle