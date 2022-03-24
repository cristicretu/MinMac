# MinMac

This repository aims to cover the basics configuration of a new Mac. It can be used as a reference for installing and setting up environments/languages/libraries.

The overall theme is **minimal** as _a clean computer offers clean thoughts_.

## Contributing

Feel free to contribute to this project using our (contribution template!!!!!!!!!)[].

# Table of Contents

- [System Preferenes](#system-preferences)
- [Xcode](#xcode)
- [Homebrew](#homebrew)

# System Preferences

Optional but highly suggested changes:

## General

- Show scroll bars
  - When scrolling
- Prefer tabs
  - always when opening documents

## Dock & Menu Bar

> _Minimal_

- Size
  - 15%
- Magnification
  - On & 25%
- Minimise windows using
  - Genie effect
- Menu bar
  - Show only the Control Centre (& battery status), as all the settings are already there and they wouldn't clutter the menu bar.
  - (image)[]

## Notifications & Focus

- Notifications
  - All off

## Users & Groups

- Login Items
  - Make sure to remove everything from here

## Security & Privacy

> Highly important

- General
  - Require password _*immediately*_ after sleep or screen saver begins
  - Disable automatic login
  - Allow apps downloaded from:
    - App Store and identified developers
- Firewall
  - On
  - Firewall options
    - Untick _Automatically allow built-in software to receive incoming connections_
    - Untick _Automatically allow downloaded signed software to receive incoming connections_
    - Tick _Enable stealth mode_
- Privacy
  - Make sure to remove all apps that wouldn't need your private info. (i.e Linear needing your location).

## Keyboard

- Keyboard
  - Key Repeat
    - Fast (Vim)
  - Delay Until Repeat
    - Short (Vim)
  - Use F1, F2, etc. keys as standars function keys
- Text
  - Add shorcuts such as _'@@' -> 'tim@apple.com'_

## Trackpad

- Point & Click
  - Enable Tap to click
  - Enable Secondary Click

# Xcode

Xcode is an integrated development environment for macOS containing a suite of software development tools developed by Apple for developing software for macOS, iOS, watchOS, and tvOS.

You can download it from the [App Store](https://apps.apple.com/us/app/xcode/id497799835?mt=12) or from [Apple's website](https://developer.apple.com/xcode/).

Most of the development tools rely on the Xcode command-line tools:

```bash
# use this to install them
xcode-select --install
```

# Homebrew

Homebrew calls itself "The missing package manager for macOS" and is oftentimes used to install different apps as you do on Linux (i.e apt install .../ pacman -S ... )

## Installation

> Make sure to have [Xcode command line tools](#xcode) installed first.

```bash
sudo xcode-select --install
```

Then use the following script to install Homebrew

```bash
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install.sh)"
```

## Path

To make the Homebrew-installed packages available to your shell, you need to add your Homebrew location to your `$PATH`.

Use this command to add it to your bash profile (zsh, fish, or other shell guides are available on google)

```bash
echo 'PATH="/usr/local/bin:$PATH"' >> ~/.bash_profile
```

Then to make sure it works, run

```bash
brew doctor
```

That's it!

Install apps using

```bash
brew install <formula>
```

Update formulaes with

```bash
brew update
```

> Note: If that command fails you can manually download the directory of formulas like this:

```bash
cd /usr/local/Homebrew/
git fetch origin
git reset --hard origin/master
```

To see a list of outdated apps use:

```bash
brew outdated
```

Homebrew keeps older versions of formulas installed on your system, in case you want to roll back to an older version. That is rarely necessary, so you can do some cleanup to get rid of those old versions:

```bash
brew cleanup
```

If you want to see what formulae Homebrew would delete without actually deleting them, you can run:

```bash
brew cleanup --dry-run
```

To see what you have installed (with their version numbers):

```bash
brew list --versions
```

To search for formulas you run:

```bash
brew search <formula>
```

To get more information about a formula you run:

```bash
brew info <formula>
```

To uninstall a formula you can run:

```bash
brew uninstall <formula>
```

## Casks

Homebrew-Cask extends Homebrew and allows you to install large binary files via a command-line tool. You can for example install applications like Google Chrome, Dropbox, VLC, and Spectacle. No more downloading .dmg files and dragging them to your Applications folder!

### Search

Search to see if your desired app is available as a Cask using:

```bash
brew search <package>
```

Here is an example:

```bash
brew install --cask docker
```
