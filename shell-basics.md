   # Shell basics

   ## Reading the prompt
   ghostgrid@nightshade:~$  → user @ host : current folder, $ = normal user (# = root)

   ## Command grammar
   command -option value argument
   - Short options: -t, -la (can combine)
   - Long options: --global, --list
   - Subcommands: git config, git add, dnf install
   - Spaces split words. Quote anything with a space: "like this"

   ## Paths
   /  = top of filesystem   ~  = home (/home/ghostgrid)
   .  = this folder         .. = one folder up
   .name = hidden (see with ls -a)

   ## Variables
   $USER  $HOME  $HOSTNAME  $PATH
   - Make one: name="value" (no spaces around =)
   - Use it: echo "$name"
   - "command not found" = not in any folder listed in $PATH

   ## Prompts
   [y/N]     capital letter = default if you press Enter
   Password: typing is hidden on purpose
   (...)     value in brackets = default, press Enter to accept

   ## Finding help
   man cmd       full manual (q to quit, /word to search)
   cmd --help    short summary
   type cmd      what a command is and where it lives
   man -k word   find commands by topic
   dnf search / dnf info   find software before installing
   history | grep word, Ctrl+R   find commands I've run before

   ## Konsole
   Copy: Ctrl+Shift+C   Paste: Ctrl+Shift+V
   Ctrl+C = stop the running command

   ## Symbols
   |  pipe: send one command's output into another
   <  feed a file into a command
   *  wildcard: matches anything

   ## Git routine
   git status                what's changed
   git add .                 stage everything changed
   git commit -m "message"   save a snapshot
   git push                  send it to GitHub

   ## SSH keys
   - id_ed25519 = private. Never share it
   - id_ed25519.pub = public. Safe to share (GitHub, servers)
   - Passphrase can't be recovered
   - Show fingerprint: ssh-keygen -lf ~/.ssh/id_ed25519.pub
