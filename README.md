# Tori releases

Official release builds of Tori, a dev workflow manager: session tree, agent
terminal, and editor in one app. Each build is attached to its entry on the
[Releases page](../../releases).

Tori is in alpha: expect fast iteration and frequent updates.

## Install with Homebrew (recommended)

```sh
brew install --cask gettori/tap/tori
```

Homebrew asks you to confirm trust for the tap the first time; confirm and
you're set. Everything is handled for you, including updates:

```sh
brew upgrade --cask tori
```

## Install from the DMG

1. Download the `.dmg` from the [Releases page](../../releases) (alpha builds
   are listed as pre-releases).
2. Drag `Tori.app` into `/Applications`.
3. Run this once so macOS opens the app right away:

```sh
xattr -cr /Applications/Tori.app
```

Alpha builds are not signed yet, which is why direct downloads take this one
extra step (Homebrew takes care of it for you). Repeat it after installing a
new version from a DMG. Signed builds will make it unnecessary.

## Sway is Tori now

The app was called Sway up to 26.914.2-alpha, and older entries on the Releases
page still carry that name. Everything moved at once: the cask is `tori`, the
tap is `gettori/tap`, and the builds live here.

Upgrading is a clean break. Tori reads none of what Sway wrote, so it opens on
first-run setup with no spaces, no settings and no signed-in hosts, and the
agent sign-ins have to be done again. Nothing is deleted: if you want Sway's
files gone, they are

- `~/.config/sway`
- `~/Library/Application Support/sway`
- `~/Library/Caches/sway`
- the `com.sway.forge` keychain entries
- `.sway/` and `refs/sway/` inside any repo Sway touched

and `Sway.app` itself, which stays in Applications until you drag it to the
Trash. Worktrees Sway made are ordinary git worktrees and are not its to
delete.
