# mac-setup

My Mac setup.

## Prerequisites

1. Create account on Mac. Provide name you wish to use with git.
2. Login to Mac App Store. Apple ID should be the email address you will use with git.

## Bootstrap

Fresh Mac? Bootstrap the setup.

This installs Homebrew (if it is not installed) and then executes Setup Mac script.

```bash
bash <(curl -s https://raw.githubusercontent.com/sutch/mac-setup/master/bootstrap-setup-mac)
```

Note: This creates a folder named mac-setup in your home directory.

## Setup Mac

Occasionally execute `setup-mac` to update software and enforce configuration.

- Adds the third-party Brew repositories in tap.txt via `brew tap`
- Installs the software listed in brew.txt via `brew install`
- Installs the software listed in cask.txt via `brew cask install`
- Installs oh-my-zsh (https://ohmyz.sh/)
- Configures zsh (see setup-mac script for details)
- Configure git
  - Populates user.name with the current user's name
  - Populates user.email with the current user's Apple ID (as logged into Mac App Store)
  - Uses Atom as core.editor
- Install Amphetamine from App Store
