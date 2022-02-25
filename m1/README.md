# m1 mac setup

## terminal setup
### rosetta
`softwareupdate --install-rosetta`

### homebrew
- `/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"`

### fish
- `brew install fish`
- add `which fish` to `/etc/shells`
- change shell `chsh -s /opt.homebrew/bin/fish`
- install omf `curl https://raw.githubusercontent.com/oh-my-fish/oh-my-fish/master/bin/install | fish`
- install bobthefish theme `omf install bobthefish`
- setup powerline fonts
    - `git clone https://github.com/powerline/fonts.git`
    - `cd fonts`
    - `./install.sh`
    - configure fonts in iterm profiles -> default -> text

### iterm2
`https://iterm2.com/`

### git
`brew install git`

### nvm
`omf install https://github.com/fabioantunes/fish-nvm`
`omf install https://github.com/edc/bass`
- add nvm.fish to ./config/fish/functions
```bash
function nvm
    bass source ~/.nvm/nvm.sh --no-use ';' nvm $argv
end
```

## ssh keys
- add ssh keys