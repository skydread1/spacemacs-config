# spacemacs-config

The current spacemacs config I am using for **mac**

If you want to get the same spacemacs setup from scratch, you can follow the steps below.

## Install Emacs Using cask

Homebrew now recommends to use the cask version with the following message: "Please try the Cask for a better-supported Cocoa version". To install the cask version:

```bash
brew install --cask emacs
```

## Install Source Code Pro font

Once Emacs is installed, spacemacs recommends to install install the default Source Code Pro font:

```bash
brew tap homebrew/cask-fonts
brew install svn
brew install --cask font-source-code-pro
```

## Install spacemacs

To get the default branch (develop), just clone the repo:
```bash
git clone https://github.com/syl20bnr/spacemacs ~/.emacs.d
```

## Emacs logo

For mac, we can change the logo from Emacs to Spacemacs by following these 2 steps:
1. [download the .icns version of the logo](https://github.com/nashamri/spacemacs-logo)
2. [change the logo on the Dock](https://www.idownloadblog.com/2014/07/16/how-to-change-app-icon-mac/)

## Cannot start emacs

On mac, you might get an error while starting Emacs for the first time saying it might be a malicious program.
You can fix it this way:

[https://support.apple.com/en-sg/guide/mac-help/mchleab3a043/mac](https://support.apple.com/en-sg/guide/mac-help/mchleab3a043/mac)

once emacs starts for the first time, just select `vim` and `spacemacs` to let emacs setup everything for you.

## Warning (evil-collection)

You might get this error right away:

```bash
Warning (evil-collection): `evil-want-keybinding' was set to nil but not before loading evil.

Make sure to set `evil-want-keybinding' to nil before loading evil or evil-collection.

See https://github.com/emacs-evil/evil-collection/issues/60 for more details. Disable showing Disable logging
```

So just added `evil-want-keybinding` to `t` in your .spacemacs `dotspacemacs/init`.

Then reload spacemacs config via the shortcut via `SPC f e R`

If the changes seem to not be applied, you can restart emacs via `SPC q r`.

## Add osx config layer

From the spacemacs readme:
**Notes:**
*After completing the Spacemacs [install process](https://github.com/syl20bnr/spacemacs#install), then it's also recommended to add the [osx layer](https://develop.spacemacs.org/layers/+os/osx/README.html) to your [dotfile](https://develop.spacemacs.org/doc/DOCUMENTATION#dotfile-configuration). Installation instructions are available in the documentation for the [osx layer](https://develop.spacemacs.org/layers/+os/osx/README.html).*

## ripgrep bugs

If some bugs occur with when searching in project, spacemacs recommends to download `ripgrep`

```bash
brew install ripgrep
```

## .spacemacs

You shoud now be able to custom your config.

The file is located at `~/.spacemacs`

If you like the evil mode and you are a Clojure developer, feel free to have a look at my very basic config for inspiration.
