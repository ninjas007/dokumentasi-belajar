https://stackoverflow.com/questions/67254339/nvm-install-node-fails-to-install-on-macos-big-sur-m1-chip

### Uninstalled nvm if it’s already installed using Homebrew.

```
brew uninstall nvm
brew cleanup
Install Rosetta
```

softwareupdate --install-rosetta
Make terminal/iTerm2 to open in Rosetta mode

got to Application (-> utilities) -> right click on terminal app -> get Info -> Select "Open using Rosetta" -> Restart Terminal

### In Terminal run a command

```
arch -x86_64 zsh 
Make sure machine has .zshrc file if not just create one
```

```
cd ~
touch .zshrc
```

### Install NVM

```
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.0/install.sh | bash
```

Restart the terminal and check if nvm is installed successfully by running

```
nvm -v
Then install Node with nvm as usual
nvm install 10
```
