<img src="https://mkitt.net/apple-touch-icon.png" width="80px" height="80px" />

# dotfiles

My personal dotfiles for macOS. Tuned to work with Apple's Terminal.app

&hearts; the Vim.

## Commands

The main tasks are `Makefile` targets. To see the available commands provided by
the `install`, `uninstall`, `update` and `help` scripts run:

```
make help
```

## Tips

### Git credentials

To setup your git credentials you'll need to add a `.gitconfig.local` file to
your `$HOME` directory and add the following:

```
[user]
  name = YOUR_GIT_AUTHOR_NAME
  email = YOUR_GIT_AUTHOR_EMAIL
  signingKey = YOUR_GIT_SIGNING_KEY
[github]
  user = YOUR_GITHUB_USERNAME
```

Note: Git will ignore `*.local` files. The `install`/`uninstall` script
symlinks/removes a `gitconfig.local`.

### GPG

Install GPG Keychain for GPG signing to happen automatically. See [GPG
Tools][gpg_tools] for more information. To get your GPG signing key you can
either open up GPG Keychain, or run `gpg --list-keys` and add this to in your
`.gitconfig.local` file. If you are transferring a key to a new computer
see [the knowledge base article][gpg_transfer]

### Install Terminal.app themes

Included in the vimrc is `Plug mkitt/pigment`. This is the color settings for
Vim. Any color profile should work with this theme including the defaults from
Apple. Included from the [pigment][pigment] repository is the Polarized light
and dark profiles. Import these profiles into Apple's Terminal.app and set one
as the default. The location of the profiles is:

```
~/.vim/plugged/pigment/profiles/
```

### Migrating to a new machine

1. Setup iCloud
2. Download App store applications
3. Run `xcode-select --install`
4. Install [homebrew][homebrew]
5. Run `brew install git hub`
6. Run `git clone mkitt/dotfiles && cd dotfiles`
7. Add the `.gitconfig.local` file
8. Run `make install`
9. Follow post install instructions (Vim plugins)
10. Install Terminal colors
11. Map caps lock to the control key
12. Set other reasonable [macOS defaults][macos_defaults]
13. Setup SSH & GPG keys (see account settings in GitHub)
14. Pull down key repositories
15. [Wipe old computer][wipe]

---

[mkitt.net][mkitt.net] | [github/mkitt][github]

<!-- Markdown links -->

[github]: https://github.com/mkitt "github.com/mkitt"
[gpg_tools]: https://gpgtools.org/ "gpg tools"
[gpg_transfer]: https://gpgtools.tenderapp.com/kb/gpg-keychain-faq/backup-or-transfer-your-keys "transfer gpg"
[homebrew]: https://brew.sh "homebrew's home"
[macos_defaults]: http://mths.be/macos "macos defaults"
[mkitt.net]: https://mkitt.net "🏔"
[pigment]: https://github.com/mkitt/pigment "vim and bash colors"
[wipe]: https://support.apple.com/en-us/HT201065 "wipe"
