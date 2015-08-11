# Super Awesome Workstation Bootstrap
Easily provision your OS X workstation into a development machine.

The setup can be run multiple times on the same machine safely. It installs, upgrades, or skips packages based on what is already installed on the machine.

## Install

Simply run the setup:

```console
$ ./setup
```

Review the steps the setup is going to take and confirm with `y`, `Y`, `yes` or `YES` to continue. 

If you want to setup an even better development machine, you can also use my [OS X Settings](https://github.com/kevintuhumury/osx-settings) and my [Vim Settings](https://github.com/kevintuhumury/vim-settings).

## What does it do?

1. Install, update and configure Homebrew.
2. Install or upgrade the Homebrew formulas:
    - zsh
    - git
    - macvim
    - postgres
    - sqlite
    - redis
    - ack
    - wget
    - openssl
    - libyaml
    - imagemagick
    - readline
3. Configure zsh as the default shell.
4. Install RVM.
5. Install the configured Rubies and set the default version.
6. Install Bundler and upgrade to the latest Rubygems version.
7. Install Homebrew Cask.
8. Install or upgrade the list of OS X applications using Homebrew Cask:
	  - 1password
    - alfred
    - appcleaner
    - coconutbattery
    - daisydisk
    - dropbox
    - evernote
    - flux
    - githubpulse
    - rowanj-gitx
    - hipchat
    - iterm2
    - karabiner
    - mou
    - slack
    - spectacle
    - spotify
    - virtualbox
    - vagrant

9. Configure OS X specific settings.
10. Run any setup from ~/.workstation.local.

## Customize in `~/.workstation.local`

Your `~/.workstation.local` is run at the end of the setup.
Put your customizations there.

## Credits

This is heavily inspired by others, but mostly by [@thoughtbot](https://github.com/thoughtbot/laptop).
