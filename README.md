# MinMac

This repository aims to cover the basics configuration of a new Mac. It can be used as a reference for installing and setting up environments/languages/libraries.

The overall theme is **minimal** as _a clean computer offers clean thoughts_.

## Contributing

Feel free to contribute to this project using our (contribution template!!!!!!!!!)[].

# Table of Contents

- [System Preferenes](#system-preferences)
- [Xcode](#xcode)

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

Xcode is an integrated development environment for macOS containing a suite of software development tools developed by Apple for developing software for macOS, iOS, watchOS and tvOS.

You can download it from the [App Store](https://apps.apple.com/us/app/xcode/id497799835?mt=12) or from [Apple's website](https://developer.apple.com/xcode/).

Most of the development tools rely on the Xcode command line tools:

```bash
# use this to install them
xcode-select --install
```
