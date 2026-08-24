# Sway releases

Release binaries for Sway. The source lives in a private repository; this repo
holds only the built artifacts and install instructions.

Sway is currently in alpha and the builds are unsigned. macOS will refuse a
plain download with a "damaged" dialog unless you install through one of the
paths below.

## Install with Homebrew (recommended)

```sh
brew tap skarif2/tap
brew install --cask sway --no-quarantine
```

The `--no-quarantine` flag matters: without it macOS quarantines the app and
refuses to open it. Upgrades keep working the usual way:

```sh
brew upgrade --cask sway --no-quarantine
```

## Install from the DMG

1. Download the `.dmg` from the [latest release](../../releases/latest).
2. Drag `Sway.app` to `/Applications`.
3. Clear the quarantine attribute:

```sh
xattr -cr /Applications/Sway.app
```

Without step 3, macOS reports the app as damaged. This goes away once builds
are signed and notarized.
