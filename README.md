# mac-setup

My Mac setup.

## Bootstrap

Fresh Mac? Bootstrap the setup.

Installs Homebrew (if it is not installed) and then executes setup-mac.

Note: This creates a folder named mac-setup in your home directory.

```bash
bash <(curl -s https://raw.githubusercontent.com/sutch/mac-setup/master/bootstrap-setup-mac)
```

## Setup Mac

- Installs the software listed in brew.txt via `brew`
- Installs the software listed in cask.txt via `brew cask
