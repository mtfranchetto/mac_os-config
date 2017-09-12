# macOS config

[![Circle CI Status](https://circleci.com/gh/bkuhlmann/mac_os-config.svg?style=svg)](https://circleci.com/gh/bkuhlmann/mac_os-config)
[![Patreon](https://img.shields.io/badge/patreon-donate-brightgreen.svg)](https://www.patreon.com/bkuhlmann)

Shell scripts for customized macOS machine setup and configuration.

This project provides a highly opinionated default configuration built upon the
[macOS](https://github.com/bkuhlmann/mac_os) project. Should the configuration provided by this
project not be to your liking, feel free to fork and customize for your specific needs.

<!-- Tocer[start]: Auto-generated, don't remove. -->

## Table of Contents

  - [Features](#features)
  - [Requirements](#requirements)
  - [Setup](#setup)
  - [Usage](#usage)
    - [Customization](#customization)
  - [Additional Software](#additional-software)
    - [Post Install](#post-install)
  - [Versioning](#versioning)
  - [Code of Conduct](#code-of-conduct)
  - [Contributions](#contributions)
  - [License](#license)
  - [History](#history)
  - [Credits](#credits)

<!-- Tocer[finish]: Auto-generated, don't remove. -->

## Features

- Downloads, installs, and configures [Homebrew Formula](http://brew.sh) command line software:
    - [Readline](http://tiswww.case.edu/php/chet/readline/rltop.html)
    - [OpenSSL](https://openssl.org)
    - [Colorized Cat](https://github.com/jingweno/ccat)
    - [diff-so-fancy](https://github.com/so-fancy/diff-so-fancy)
    - [Git](http://git-scm.com)
    - [Go](http://golang.org)
    - [hr](https://github.com/LuRsT/hr)
    - [htop](http://hisham.hm/htop)
    - [HTTPie](https://github.com/jkbrzt/httpie)
    - [mas](https://kapeli.com/app_store_migrate)
    - [Node.js](http://nodejs.org)
    - [Peco](https://github.com/peco/peco)
    - [Redis](http://redis.io)
    - thefuck
    - Terraform
    - [Tree](http://mama.indstate.edu/users/ice/tree)
    - [Yarn](https://yarnpkg.com)
    - [Z](https://github.com/rupa/z)
    - zsh
    - zsh-completions
    - Oh my zsh
- Downloads, installs, and configures [Homebrew Cask](https://caskroom.github.io) command line
  software:
    - [App Cleaner](http://www.freemacsoft.net/appcleaner)
    - Bartender
    - [Dash](http://kapeli.com/dash)
    - [Dropbox](https://www.dropbox.com)
    - [Firefox](http://www.mozilla.com/en-US/firefox)
    - [Google Chrome](http://www.google.com/chrome)
    - [ImageOptim](http://imageoptim.pornel.net)
    - [iStat Menus](https://bjango.com/mac/istatmenus)
    - [iTerm2](http://www.iterm2.com)
    - [Marp](https://yhatt.github.io/marp)
    - Karabiner elements
    - [QLStephen](https://whomwah.github.io/qlstephen)
    - [RescueTime](https://www.rescuetime.com)
    - Sourcetree
    - [Sublime Text 3](http://www.sublimetext.com)
    - [Trailer](http://ptsochantaris.github.io/trailer)
    - [Visual Studio Code](https://code.visualstudio.com)
    - VirtualBox
    - [VLC](http://www.videolan.org/vlc)
- Downloads, installs, and configures
    [App Store](http://www.apple.com/macosx/whats-new/app-store.html) applications.
    - [CCMenu](http://ccmenu.org)
    - [Day One](http://dayoneapp.com)
    - Enpass
    - [Kindle](http://www.amazon.com/gp/feature.html?docId=1000464931)
    - Next meeting
    - [Slack](https://slack.com)
    - Telegram
    
## Requirements

[macOS](https://github.com/bkuhlmann/mac_os)

## Setup

Open a terminal window and execute one of the following setup sequences depending on your version
preference:

Current Version (stable):

    git clone https://github.com/bkuhlmann/mac_os-config.git
    cd mac_os-config
    git checkout v3.1.0

Master Version (unstable):

    git clone https://github.com/bkuhlmann/mac_os-config.git
    cd mac_os-config

## Usage

See the [macOS](https://github.com/bkuhlmann/mac_os) project for usage as it provides the command
line interface to the configuration defined by this project.

### Customization

While this project's configuration is opinionated and tailored for my setup, you can easily fork
this project and customize it for your environment. Start by editing the files found in the `bin`
and `lib` directories. Here is a breakdown of each:

- `bin/apply_basic_settings`: Applies basic and initial settings for setting up a machine.
- `bin/apply_default_settings`: Applies useful system and application defaults.
- `bin/install_app_store`: Installs macOS, GUI-based, App Store applications.
- `bin/install_applications`: Installs macOS, GUI-based, non-App Store applications.
- `bin/install_extensions`: Installs macOS application extensions and add-ons.
- `bin/install_homebrew_casks`: Installs Homebrew Casks.
- `bin/install_homebrew_formulas`: Installs Homebrew Formulas.
- `bin/restore_backup`: Restores system/application settings from backup image.
- `bin/setup_software`: Configures and launches (if necessary) installed software.
- `lib/settings.sh`: Defines custom settings for software applications, extensions, etc.

*TIP*: The installer determines which applications/extensions to install as defined in the
`settings.sh` script. Applications defined with the "APP_NAME" suffix and extensions defined with
the "EXTENSION_PATH" suffix inform the installer what to care about. Removing/commenting out these
applications/extensions within the `settings.sh` file will cause the installer to skip these
applications/extensions.

## Additional Software

### Post Install

The following are additional steps, not easily automated, that are worth completing after the
install scripts have been executed:

- Lauch App Store and install all purchased software and other things.
  - Airmail 
	- Alfred
	- Spectacle
  - Contexts
	- Oh my zsh
	- Macdown
	- Focus
	- uTorrent
	- Charles
	- Skype
- Configure System Preferences:
  - Security & Privacy:
    - General:
      - Require password immediately after sleep or screen saver begins.
      - Enable message when screen is locked. Example: `<twitter> | <email> | <phone> | <url>`.
      - Allow your Apple Watch to unlock your Mac.
    - FileVault:
      - Enable FileVault and save the recovery key in a secure location (i.e. 1Password).
    - Firewall:
      - Enabled it.
      - Automatically allow signed software.
      - Enable stealth mode.
    - Privacy:
      - Apps like Cheat Sheet, Dash, Dropbox, Trailer, etc. will need to be enabled for
        accessibility.
  - Printers & Scanners:
    - Add printer/scanner.
  - iCloud:
    - Enable Find My Mac.
  - Internet Accounts:
    - Add all accounts used by Mail.
  - Network:
    - Configure Wi-Fi.
  - Users & Groups:
    - Update avatar.
    - Remove unused login items.
    - Disable guest account.

## Versioning

Read [Semantic Versioning](http://semver.org) for details. Briefly, it means:

- Major (X.y.z) - Incremented for any backwards incompatible public API changes.
- Minor (x.Y.z) - Incremented for new, backwards compatible, public API enhancements/fixes.
- Patch (x.y.Z) - Incremented for small, backwards compatible, bug fixes.

## Code of Conduct

Please note that this project is released with a [CODE OF CONDUCT](CODE_OF_CONDUCT.md). By
participating in this project you agree to abide by its terms.

## Contributions

Read [CONTRIBUTING](CONTRIBUTING.md) for details.

## License

Copyright (c) 2016 [Alchemists](https://www.alchemists.io).
Read [LICENSE](LICENSE.md) for details.

## History

Read [CHANGES](CHANGES.md) for details.
Built with [Bashsmith](https://github.com/bkuhlmann/bashsmith).

## Credits

Developed by [Brooke Kuhlmann](https://www.alchemists.io) at
[Alchemists](https://www.alchemists.io).
