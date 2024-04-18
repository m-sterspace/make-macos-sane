# make-macos-sane
A series of steps and/or scripts to modify MacOS into a usable OS for a developer coming from Windows.

## Steps:

1. Go to Settings > Keyboard > Keyboard Shortcuts > Modifer Keys and change `Command` to `Control`, `Control` to `Command`, and `Global` to `Command`. Repeat for any external keyboards. This will adjust most keyboard shortcuts to mirror Windows'.
2. Go to `Settings > Trackpad` and enable `Tap to click`
3. Go to `Settings > Desktop & Dock` and change `Click wallpaper to reveal desktop` to `Only in Stage Manager`
4. Use Safari to download a better browser then close it and never open it again
   * Go to `Settings > Default Web Browser` and change it to your new one
5. Remove all the Apple programs from the taskbar except Finder
6. Run this so that you can see hidden files and folders in Finder: `defaults write com.apple.finder AppleShowAllFiles -boolean true; killall Finder;`
7. [Install Homebrew](https://brew.sh/) so that you can install the other stuff you need
8. [Install middleclick-sonoma](https://github.com/artginzburg/MiddleClick-Sonoma) so that the trackpad supports three finger middleclick like it's 2012
   * Run it, follow the prompt to give it access in settings, then in the top right click it to enable `Tap to click`
9. [Install rectangle](https://rectangleapp.com/) so that windows can be snapped to the side like it's 2015
    * Run it, follow the prompt to give access in settings, then remap all the default combos. They're set to Control + Option + `X` which is the closest you'll get to Windows, but since you switched your command and control key you'll need to switch them here.
10. [Install BetterDisplay](https://betterdisplay.pro/) so that you can control external monitor scaling like it's 2003. 
11. [Install the Cascadia Code](https://github.com/microsoft/cascadia-code/releases) font so that you can dare to have ligatures. Unzip > Open TTF folder > Double click `Cascadia Code.ttf`. You may then have to restart your computer before it shows up in font book.
12. [Install kitty](https://sw.kovidgoyal.net/kitty/binary/#binary-install) so that your terminal is GPU rendered like it's 2019
    * Configure Cascadia code font by going to `~/.config/kitty/`, open `kitty.conf` and add the following line: `font_family Cascadia Code`
13. [Install VS Code](https://code.visualstudio.com/Download) or [VS Codium](https://vscodium.com/).
    * install using brew so that it adds code to the terminal:
      * `brew install --cask visual-studio-code`
      * -or- `brew install --cask vscodium`
    * Enable Cascadia Code & ligature support in `Settings > Font > Font Family`, and `Settings > Enable Ligatures`
14. [Install git](https://git-scm.com/download/mac), use brew
15. [Install git credential manager](https://github.com/git-ecosystem/git-credential-manager/blob/release/docs/install.md), use brew
16. Install [NVM](https://nvm.sh/) to manage Node versions.
17. Install [sdkman](https://sdkman.io/) to manage Java versions.
18. Install [RVM](https://rvm.io/) to manage Ruby versions.
19. Install [XCode](https://apps.apple.com/us/app/xcode/id497799835?mt=12) / [Android Studio](https://formulae.brew.sh/cask/android-studio) if doing native or React Native Development.
20. Open Finder, right click `desktop` > `add to dock`, then right click the dock icon and change `View content as` to `Fan` and `Sort by` to `Date Modified` so that you have access to screenshots
