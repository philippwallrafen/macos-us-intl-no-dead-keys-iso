# macOS US International without dead keys — ISO fixes

A fork of [dnnspaul/macos-us-intl-no-dead-keys](https://github.com/dnnspaul/macos-us-intl-no-dead-keys) with corrected mappings for ISO keyboards.

The original layout provides a US International keyboard layout for macOS without the usual dead-key behavior.

This fork keeps the original layout intact except for a small set of corrections related to the additional key present on ISO keyboards.

## Why this fork exists

On ISO keyboards, macOS distinguishes between two physical keys:

- the grave/tilde key
- the additional ISO `non_us_backslash` key

In the version this fork is based on, both keys were mapped to the same characters:

| Key | Normal | Shift |
|---|---|---|
| `non_us_backslash` | `` ` `` | `~` |
| grave/tilde | `` ` `` | `~` |

This made the ISO key effectively unusable for typing `\` and `|`.

This fork changes the mappings to:

| Key | Normal | Shift |
|---|---|---|
| `non_us_backslash` | `\` | `|` |
| grave/tilde | `` ` `` | `~` |

## Changes

The keyboard layout itself is unchanged apart from the following corrections:

- Map the ISO `non_us_backslash` key to `\`
- Map Shift + `non_us_backslash` to `|`
- Apply the corresponding correction to Caps Lock, Option, Command, and Control modifier maps
- Keep the actual grave/tilde key mapped to `` ` `` and `~`
- Correct Caps Lock behavior for the grave/tilde key
- Remove one remaining grave dead-key action from the alternate keyboard map

In total, 12 lines of the original `.keylayout` file were changed.

## Installation

Copy the keyboard layout bundle to:

```text
~/Library/Keyboard Layouts/
