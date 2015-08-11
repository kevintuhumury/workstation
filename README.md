# Super Awesome OSX Workstation Setup
Easily provision your OS X workstation into a development machine.

The setup can be run multiple times on the same machine safely. It installs, upgrades, or skips packages based on what is already installed on the machine.

## Installation

Run the following to provision your OS X workstation:

``` bash
./setup
```

Review the steps the setup is going to take and confirm with `y`, `Y`, `yes` or `YES` to continue.

If you want to setup an even better development machine, you can also use my [OSX Settings](https://github.com/kevintuhumury/osx-settings) and my [Vim Settings](https://github.com/kevintuhumury/vim-settings).

## What does it do?

1. Install, update and configure [Homebrew](http://brew.sh/).
2. Install or upgrade the Homebrew formulas:
    - [ZSH](http://www.zsh.org/)
    - [Git](https://git-scm.com/)
    - [Ack](http://beyondgrep.com/)
    - [MacVim](https://github.com/b4winckler/macvim)
    - [Postgres](http://www.postgresql.org/)
    - [SQLite](https://www.sqlite.org/)
    - [Redis](http://redis.io/)
    - [OpenSSL](https://www.openssl.org/)
    - [ImageMagick](http://www.imagemagick.org/)
    - [QT](http://www.qt.io/developers/)
3. Configure ZSH as the default shell.
4. Install [RVM](https://rvm.io/).
5. Install the configured Rubies and set the default version.
6. Install [Bundler](http://bundler.io/) and upgrade to the latest [Rubygems](https://rubygems.org/) version.
7. Install [Homebrew Cask](http://caskroom.io/).
8. Install or upgrade the list of OS X applications using Homebrew Cask:
    - [1password](https://agilebits.com/onepassword)
    - [Alfred](https://www.alfredapp.com/)
    - [AppCleaner](http://www.freemacsoft.net/appcleaner/)
    - [coconutBattery](http://www.coconut-flavour.com/coconutbattery/)
    - [DaisyDisk](http://www.daisydiskapp.com/)
    - [Dropbox](https://www.dropbox.com/)
    - [Evernote](https://evernote.com/)
    - [f.lux](https://justgetflux.com/)
    - [Github Pulse](https://github.com/tadeuzagallo/GithubPulse)
    - [GitX](http://rowanj.github.io/gitx/) (by rowanj)
    - [HipChat](https://www.hipchat.com/)
    - [iTerm 2](https://www.iterm2.com/)
    - [Karabiner](https://pqrs.org/osx/karabiner/)
    - [Mou](http://25.io/mou/)
    - [Slack](https://slack.com/)
    - [Spectacle](http://spectacleapp.com/)
    - [Spotify](https://www.spotify.com/)
    - [VirtualBox](https://www.virtualbox.org/)
    - [Vagrant](https://www.vagrantup.com/)
9. Configure OS X specific settings.
10. Run any setup from ~/.workstation.local.

## Configuration

This setup installs several Ruby versions using RVM, see `RUBY_VERSIONS` in `sh/configuration`. It also (amongst other things) sets a different default screen capture location (see `DEFAULT_SCREENCAPTURE_LOCATION`). To change any of these settings, go ahead and adjust the `sh/configuration` file to your liking.

## Customizing the setup

The `~/.workstation.local` file (the location of this file can also be changed in `sh/configuration`) is run at the very end of the setup. If you want to add any additional packages (Homebrew formulas) or OS X applications, you can add them to that file using the `brew_install_or_upgrade` and `cask_install_or_upgrade` functions.

The helper functions `title`, `info`, `fail` and `success` can also be used for nicely colored output. For example:

```sh
#!/bin/bash

title "Google Chrome"
info "Installing Google Chrome"

cask_install_or_upgrade "google-chrome"
success "Google Chrome has been installed."
```

## Credits

This is heavily inspired by others, but mostly by [@thoughtbot](https://github.com/thoughtbot/laptop).
