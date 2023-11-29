# make-macos-sane
A series of steps and/or scripts to modify MacOS into a usable OS for a developer coming from Windows.

## Steps:

1. Go to Settings > Keyboard > Keyboard Shortcuts > Modifer Keys and change `Command` ➡️ `Control`, `Control` ➡️ `Command`, and `Global` ➡️ `Command`. Repeat for any external keyboards. This will adjust most keyboard shortcuts to mirror Windows'.
2. Go to `Settings > Trackpad` and enable `Tap to click`
3. Go to `Settings > Desktop & Dock` and change `Click wallpaper to reveal desktop` to `Only in Stage Manager`
4. Use Safari to download a better browser then close it and never open it again
5. Remove all the Apple programs from the taskbar except Finder
6. [Install Homebrew](https://brew.sh/) so that you can install the other stuff you need
7. [Install middleclick-sonoma](https://github.com/artginzburg/MiddleClick-Sonoma) so that the trackpad supports three finger middleclick like it's 2012
   * Run it, follow the prompt to give it access in settings, then in the top right click it to enable `Tap to click`
9. [Install rectangle](https://rectangleapp.com/) so that windows can be snapped to the side like it's 2015
    * Run it, follow the prompt to give access in settings, then remap all the default combos. They're set to Control + Option + `X` which is the closest you'll get to Windows, but since you switched your command and control key you'll need to switch them here.
11. [Install the Cascadia Code](https://github.com/microsoft/cascadia-code/releases) font so that you can dare to have ligatures. Unzip > Open TTF folder > Double click `Cascadia Code.ttf`
12. [Install kitty](https://sw.kovidgoyal.net/kitty/binary/#binary-install) so that your terminal is GPU rendered like it's 2019
    * Configure Cascadia code font by going to `~/.config/kitty/`, open `kitty.conf` and add the following line: `font_family Cascadia Code`
13. [Install VS Code](https://code.visualstudio.com/Download) or [VS Codium](https://vscodium.com/).
    * Enable Cascadia Code & ligature support in `Settings > Font > Font Family`, and `Settings > Enable Ligatures`
14. [Install git](https://git-scm.com/download/mac), use brew
15. [Install git credential manager](https://github.com/git-ecosystem/git-credential-manager/blob/release/docs/install.md), use brew
16. Open Finder, right click `desktop` > `add to dock`, then right click the dock icon and change `View content as` to `Fan` and `Sort by` to `Date Modified` so that you have access to screenshots
