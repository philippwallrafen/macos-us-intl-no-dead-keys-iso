![Keyboard layout](KeyboardLayout.png)

# macOS US International — No Dead Keys for ISO Keyboards

US International keyboard layout for **macOS**, with **no dead keys** and corrected mappings for **physical ISO keyboards**.

## Installation

Paste this into Terminal:

```bash
tmp="$(mktemp -d)" && \
curl -fsSL https://github.com/philippwallrafen/macos-us-intl-no-dead-keys-iso/archive/refs/heads/main.tar.gz | tar -xz -C "$tmp" && \
mkdir -p "$HOME/Library/Keyboard Layouts" && \
rm -rf "$HOME/Library/Keyboard Layouts/US Intl PC without dead keys.bundle" && \
cp -R "$tmp/macos-us-intl-no-dead-keys-iso-main/US Intl PC without dead keys.bundle" "$HOME/Library/Keyboard Layouts/" && \
rm -rf "$tmp" && \
open "x-apple.systempreferences:com.apple.Keyboard-Settings.extension"
```

Log out and back in, then select **US Intl without dead keys** in **System Settings → Keyboard → Text Input**.

The command installs the latest version and opens Keyboard settings. macOS does not provide a stable supported command-line interface for automatically selecting a newly installed custom keyboard layout.

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
