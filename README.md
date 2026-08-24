# Sway releases

Release binaries for Sway. The source lives in a private repository; this repo
holds only the built artifacts and install instructions. The app itself is
never in the file tree: each DMG is attached to its entry on the
[Releases page](../../releases).

Sway is currently in alpha and the builds are unsigned. macOS will refuse a
plain download with a "damaged" dialog unless you install through one of the
paths below.

## Install with Homebrew (recommended)

```sh
brew install --cask skarif2/tap/sway
```

Homebrew asks you to trust the tap on first use; that prompt is expected. The
cask clears macOS quarantine itself after install, so no extra flags are
needed. Upgrades work the usual way:

```sh
brew upgrade --cask sway
```

## Install from the DMG

1. Download the `.dmg` from the [latest release](../../releases) (alphas are
   marked pre-release, so they do not show under "Latest").
2. Drag `Sway.app` to `/Applications`.
3. Clear the quarantine attribute:

```sh
xattr -cr /Applications/Sway.app
```

Without step 3, macOS reports the app as damaged. This goes away once builds
are signed and notarized.
