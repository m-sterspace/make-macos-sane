# make-macos-sane
A series of steps and/or scripts to modify MacOS into a usable OS for someone coming from Windows.

## Steps:

1. Go to Settings > Keyboard > Keyboard Shortcuts > Modifer Keys and change `Command` ➡️ `Control`, `Control` ➡️ `Command`, and `Global` ➡️ `Command`. Repeat for any external keyboards.
2. Go to Settings > Trackpad and enable `Tap to click`
3. Go to Settings > Desktop & Dock and change `Click wallpaper to reveal desktop` to `Only in Stage Manager`
4. Remove all the Apple Programs from the taskbar
5. Use Safari to download a better browser then close it and never open it again
6. [Install Homebrew](https://brew.sh/) so that you can install the other stuff you need
7. [Install middleclick-sonoma](https://github.com/artginzburg/MiddleClick-Sonoma) so that the trackpad supports three finger middleclick like it's 2012
8. [Install rectangle](https://rectangleapp.com/) so that windows can be snapped to the side like it's 2015
9. [Install Cascadia Code font](https://github.com/microsoft/cascadia-code/releases) Unzip > Open TTF folder > Double click `Cascadia Code.ttf`
10. [Install kitty](https://sw.kovidgoyal.net/kitty/binary/#binary-install) so that your terminal is GPU rendered like it's 2019
  * Configure Cascadia code font by going to `~/.config/kitty/`, open `kitty.conf` and add the following line: `font_family Cascadia Code`
11. [Install VS Code](https://code.visualstudio.com/Download) or [VS Codium](https://vscodium.com/).
  * Enable Cascadia Code & ligature support in `Settings > Font > Font Family`, and `Settings > Enable Ligatures`
12. Open Finder, right click `desktop` > `add to dock`, then right click the dock icon and change `View content as` to `Fan` and `Sort by` to `Date Modified` so that you have access to screenshots
