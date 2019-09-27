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

## Manual Steps

Still have not automated these steps.

1. Make iTerm2 Default Term - Choose "Make iTerm2 Default Term" in iTerm2 menu. Possible automation:
  - Update ~/Library/Preferences/com.apple.launchservices.secure.plist to contain:
    Root (Dictionary)
    - LSHandlers (Array)
      - Item 0 (Dictionary)
        - LSHandlerRoleShell (String) = com.googlecode.iterm2
        - LSHandlerPreferredVersions (Dictionary) =
          - LSHandlerRoleShell (String) = -
        - LSHandlerContentType (String) = public.unix-executable
2. Configure configure iTerm to use fonts new font:
  - iTerm2 -> Preferences -> Profiles -> Text -> Font -> Change Font
    - Select the font Hack Regular Nerd Font Complete.
    - Also check the box for Use a different font for non-ASCII text and select the font again.
  - Possible automation:
    - Update ~/Library/Preferences/com.googlecode.iterm2.plist to contain:
      - New Bookmarks (Array)
        - Item 0 (Dictionary)
          - Ansi 5 Color (Dictionary)
            - Normal Font (String) = HackNerdFontComplete-Regular12
      - New Bookmarks (Array)
        - Item 0 (Dictionary)
          - Ansi 10 Color (Dictionary)
            - Non Ascii Font (String) = HackNerdFontComplete-Regular12
3. Set colorscheme to dark+:
  - Download: https://raw.githubusercontent.com/mbadolato/iTerm2-Color-Schemes/master/schemes/Dark+.itermcolors
  - Follow instructions at https://iterm2colorschemes.com/
