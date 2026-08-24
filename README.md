# Sway releases

Official release builds of Sway, a dev workflow manager: session tree, Claude
terminal, and editor in one app. Each build is attached to its entry on the
[Releases page](../../releases).

Sway is in alpha: expect fast iteration and frequent updates.

## Install with Homebrew (recommended)

```sh
brew install --cask skarif2/tap/sway
```

Homebrew asks you to confirm trust for the tap the first time; confirm and
you're set. Everything is handled for you, including updates:

```sh
brew upgrade --cask sway
```

## Install from the DMG

1. Download the `.dmg` from the [Releases page](../../releases) (alpha builds
   are listed as pre-releases).
2. Drag `Sway.app` into `/Applications`.
3. Run this once so macOS opens the app right away:

```sh
xattr -cr /Applications/Sway.app
```

Alpha builds are not signed yet, which is why direct downloads take this one
extra step (Homebrew takes care of it for you). Repeat it after installing a
new version from a DMG. Signed builds will make it unnecessary.
