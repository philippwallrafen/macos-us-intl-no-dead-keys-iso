# macOS US International — No Dead Keys for ISO Keyboards

US International keyboard layout for **macOS**, with **no dead keys** and corrected mappings for **physical ISO keyboards**.

![Keyboard layout](KeyboardLayout.png)

## Installation

Clone the repository:

```bash
git clone https://github.com/philippwallrafen/macos-us-intl-no-dead-keys-iso.git
cd macos-us-intl-no-dead-keys-iso
```

Install the layout:

```bash
mkdir -p "$HOME/Library/Keyboard Layouts"
cp -R "US Intl PC without dead keys.bundle" "$HOME/Library/Keyboard Layouts/"
```

Log out and back in, then enable it in:

**System Settings → Keyboard → Text Input**

## What this fixes

This project is based on [dnnspaul/macos-us-intl-no-dead-keys](https://github.com/dnnspaul/macos-us-intl-no-dead-keys), but adjusts the two keys that differ on ISO keyboards.

| Key | This layout |
|---|---|
| ISO extra key | `\` / `|` |
| Grave/tilde key | `` ` `` / `~` |

The corrected mapping is applied across the relevant modifier layers.

## AltGr / Option

The upstream US International mappings are preserved.

| Shortcut | Output |
|---|---|
| Option+A | `á` |
| Option+E | `é` |
| Option+I | `í` |
| Option+O | `ó` |
| Option+U | `ú` |
| Option+N | `ñ` |

## Intended for

- macOS
- physical ISO keyboards
- US International users
- users who want accented characters without dead keys

## Upstream

[dnnspaul/macos-us-intl-no-dead-keys](https://github.com/dnnspaul/macos-us-intl-no-dead-keys)
