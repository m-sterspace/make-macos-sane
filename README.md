# make-macos-sane
A series of steps and/or scripts to modify MacOS into a usable OS for a developer coming from Windows.

## Steps:

### Trackpad Adjustments

1. Go to `Settings > Trackpad` and
   * Go to `Point and Click` and enable `Tap to click`.
   * Go to `Scoll & Zoom` and turn off `Natural scrolling`
   * Go to `More Gestures` and
     * Turn off `Swipe Between Pages`
     * Set `Swipe Between Full Screen Applications` to `Swipe Left or Right with Four Fingers`  
2. Go to `Settings > Desktop & Dock` and change `Click wallpaper to reveal desktop` to `Only in Stage Manager`

### Finder Adjustments
3. Run this command in a terminal so that you can see hidden files and folders in Finder: `defaults write com.apple.finder AppleShowAllFiles -boolean true; killall Finder;`
4. Open Finder, and on the menu bar, hit `Finder` > `Settings` > `Advanced` > `Show all filename extensions`

### Sudo with TouchID
5. To enable TouchID with Sudo, open `/etc/pam.d/`. Copy `sudo_local.template` to `sudo_local`. Edit it using `sudo nano sudo_local`. Uncomment the line `auth sufficient pam_tid.so`. Close and save with `ctrl` + `x`, then `y`, then `Enter`.This will now tell sudo to use TouchId instead of a password.

### Homebrew
6. Sign up for an Apple developer account and download the latest version of [XCode](https://developer.apple.com/download/all/?q=xcode) before installing brew.
7. [Install Homebrew](https://brew.sh/) so that you can install the other stuff you need

### Keyboard & More Trackpad Adjustments
8. [Install middleclick by artginzburg](https://github.com/artginzburg/MiddleClick-Sonoma) so that the trackpad supports three finger middleclick.
   * `brew install --cask middleclick`
   * Run it, follow the prompt to give it access in settings, then in the top right click it to enable `Tap to click`
9. [Install Karibiner Elements](https://karabiner-elements.pqrs.org) so that you can remap your command / control / option / global keys to match a windows keyboard layout.
    * `brew install --cask karabiner-elements`
    * -Either- Manually adjust the settings:
      * Run it, follow the prompts to give access in settings, then on the internal keyboard switch
        * `fn (globe)` to `left_command`,
        * `left_command` to `left_option`,
        * `left_control` to `left_command`
        * `left_option` to `left_control`
        * `right_command` to `right_option`
        * `right_option` to `right_command`
    * -Either- Automatically import the settings:
        * Import [this json settings file](/configs/karabiner-elements/karabiner.json) by going to `Maintenance` > `Misc` > `Export & Import` > `Open config folder` and replacing the config file here.

### Windowing Adjustments
10. [Install rectangle](https://rectangleapp.com/) so that windows can be snapped
    * `brew install --cask rectangle`
    * Run it, follow the prompt to give access in settings and disable MacOS window snapping.
    * -Either- Manually adjust the settings:
      * Open  rectangle's settings and select `Launch on login` and `Check for updates automatically`
      * Then remap all the default combos. They're set to Control + Option + `X` which is the closest you'll get to Windows, but since you switched your command and control key you'll need to switch them here.
    * -Either- Automatically import the settings:
      * Import [this settings json file](/configs/rectangle/RectangleConfig.json) by going to `Settings` > `Import` and selecting it.

### Monitor Control
11. [Install BetterDisplay (free)](https://betterdisplay.pro/) or [Lunar (paid)](https://lunar.fyi) so that you can control internal / external monitor brightness.
    *   `brew install --cask `
    *   `brew install --cask lunar`
    *   Run them and give them the accessibility settings they need.
   
### Screen Recording Location
12. Hit `Command` + `Shift` + `5` to open the screen capture screen, at the bottom of the screen hit `Options` and change the default `Save To` location to a dedicated screenshot folder.

### Dock Adjustments
13. Under system `Settings` > `Dock` set position to `Left`.
14. Install [DockDoor](https://github.com/ejbills/DockDoor) so that you can have window previews in your dock and window switcher.
    * `brew install --cask dockdoor`
    * Run it, give it the accessibility settings it needs, then open it's settings and
      * Under `General`
        * Select `Launch DockDoor at login`
        * Under `Performance Profiles` select `Snappy`
        * Under `Preview Quality Profiles select `Lightweight`
      * Under Appearance
        * Set `Preview Width` to `240px`
        * Set `Spacing Scale` to `0.8`
        * Set `Position Dock Preview Controls` to `At top - Title on left, controls on right`
        * Under `Traffic Light Buttons in Previews` disable `Quit` and `Disable dock styling on traffic light buttons`
        * Set `Max Columns (Left/Right Dock)` to 1.
15. Remove all the Apple programs from the taskbar except Finder
16. Open Finder, find your screenshot folder, right click on it, `add to dock`, then right click the dock icon and change `View content as` to `Fan` and `Sort by` to `Date Modified` so that you have access to screenshots easily

### Misc
17. Use Safari to download a better browser
   * Go to `Settings > Default Web Browser` and change it to your new one
18. Install noTunes, so that Apple doesn't launch Apple Music whenever you hit the media buttons. 
    * `brew install --cask notunes`
    * Run `noTunes`
    * Go to your system `Settings` > `Login Items & Extensions` and add `noTunes` to your Login Items.

### Dev Tooling
19. [Install the Cascadia Code](https://github.com/microsoft/cascadia-code/releases) font so that you can have font ligatures.
    * -Either- Manually
      * Unzip > Open TTF folder > Double click `Cascadia Code.ttf`. You may then have to restart your computer before it shows up in font book.
    * -Either- Automatically
      * `brew install --cask font-cascadia-code`
20. [Install ghostty](https://ghostty.org) so that your terminal is GPU rendered
    * Configure Cascadia code font by opening Ghostty's settings / config and including this line: `font-family = Cascadia Code`.
21. [Install git](https://git-scm.com/download/mac)
    * `brew install git`
    * run `git config --global user.name "<USERNAME>"`
    * run `git config --global user.email "<USER.EMAIL@ADDRESS.COM>"`
22. [Install git credential manager](https://github.com/git-ecosystem/git-credential-manager/blob/release/docs/install.md)
    * `brew install --cask git-credential-manager`
23. [Install VS Code](https://code.visualstudio.com/Download) or [VS Codium](https://vscodium.com/).
    * install using brew so that it adds code to the terminal:
      * `brew install --cask visual-studio-code`
      * -or- `brew install --cask vscodium`
    * Enable Cascadia Code & ligature support in `Settings > Font > Font Family`, and `Settings > Enable Ligatures`
    * Go to `Settings` > `Open Files In New Window` and set to `On`.

#### Node.js
20. Install [NVM](https://nvm.sh/) to manage Node versions.
    * Use the installation script they provide.

#### Java
22. Install [sdkman](https://sdkman.io/) to manage Java versions.
    * Use the installation script they provide.

#### Ruby
24. Install [ruby-build](https://github.com/rbenv/ruby-build) and [rbenv](https://github.com/rbenv/rbenv) to manage Ruby versions.
    * `brew install ruby-build`
    * `brew install rbenv`


