# mac-setup

My Mac setup.

Note: Must sign in to the App Store.

## Bootstrap

Fresh Mac? Bootstrap the setup.

Installs Homebrew (if it is not installed) and then executes setup-mac.

Note: This creates a folder named mac-setup in your home directory.

```bash
bash <(curl -s https://raw.githubusercontent.com/sutch/mac-setup/master/bootstrap-setup-mac)
```

## Setup Mac

Execute `setup-mac` occasionally.

- Adds the third-party Brew repositories in tap.txt via `brew tap`
- Installs the software listed in brew.txt via `brew install`
- Installs the software listed in cask.txt via `brew cask install`
- Installs oh-my-zsh (https://ohmyz.sh/)
- Install Amphetamine from App Store
