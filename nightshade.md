# nightshade build log

## 23/09/2026: Fedora Install
- Machine: MAcbook Air M1, 8GB RAM, 256GB Drive
- Erased MacOS, reinstalled clean
- Installed Fedora Asahi Remix 44 (KDE Plasma) with the Asahi installer via MacOS Terminal.
- Partitions: macOS 70 GB, Fedora the rest
- User: ghostgrid, hostname: nightshade
- Installed git, vim, tmux, htop, tree, curl, wget, python3-pip
- Configured Git and created an ed25519 SSH key

## 23/09/2026: Git and GitHub setup
- Git config: user.name, user.email, init.defaultBranch main
- SSH key: ed25519, stored in ~/.ssh (id_ed25519 = private, id_ed25519.pub = public)
- Added public key to GitHub as "nightshade" (Authentication Key)
- Test: ssh -T git@github.com → "successfully authenticated"@
- Created runbooks repo on GitHub, connected with git remote add origin, pushed with git push -u origin main

### Problems and fixes
- `gitconfig` → command not found. Fix: needs a space, `git config`
- `init.defaultBranchmain` did nothing. Fix: space between setting and value, `init.defaultBranch main`
- GitHub rejected the key ("invalid OpenSSH format") after copying by hand.
- Fix: `wl-copy < ~/.ssh/id_ed25519.pub`, then paste
