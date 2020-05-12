# new-machine-setup
This guide is used for setting up the development environment for a brand new machine (OSX)

## oh my zsh

### Mac OS: xcrun: error: invalid active developer path, missing xcrun
```https://ma.ttias.be/mac-os-xcrun-error-invalid-active-developer-path-missing-xcrun/```

### Set up spaceship/customized theme on oh my zsh
Clone this repo:
```
git clone https://github.com/denysdovhan/spaceship-prompt.git "$ZSH_CUSTOM/themes/spaceship-prompt"
```

Symlink spaceship.zsh-theme to your oh-my-zsh custom themes directory:
```
ln -s "$ZSH_CUSTOM/themes/spaceship-prompt/spaceship.zsh-theme" "$ZSH_CUSTOM/themes/spaceship.zsh-theme"
```

Set the zsh theme in .zshrc:
```
ZSH_THEME="spaceship"
```

Go to .oh-my-zsh/custom/themes/spaceship.zsh and override the custom spaceship_zsh-theme

Install powerline font:

clone
```
git clone https://github.com/powerline/fonts.git --depth=1
```
install
```
cd fonts
./install.sh
```

clean-up a bit
```
cd ..
rm -rf fonts
```

## Show hidden files
```
Cmd + Shift + .
```

## Install nvm
https://github.com/nvm-sh/nvm

Add this to `.zshrc` if it's not already there

```
export NVM_DIR="$([ -z "${XDG_CONFIG_HOME-}" ] && printf %s "${HOME}/.nvm" || printf %s "${XDG_CONFIG_HOME}/nvm")"
[ -s "$NVM_DIR/nvm.sh" ] && \. "$NVM_DIR/nvm.sh" # This loads nvm
```

### zsh compinit: insecure directories and files
https://github.com/zsh-users/zsh-completions/issues/680

### unable to access global packages installed when switching between different versions of node
```
npm link [packagen name]
npm link @angular/cli
```

## Install Docker

## Vscode

### Download Extension: "Settings Sync" by Shan Khan
Login with github and upload gist file

Lavie's settings Gist: https://gist.github.com/Lavioli/1b2c62b076434d98f7a8244274793ecb

### Check if git is installed:
```
git --version
```

### Check if node is installed:
```
node -v
```
If not, use nvm and download the latest version
```
nvm ls-remote
nvm install [version]
```

## Mongodb Installation

### Installing with brew
https://medium.com/better-programming/installing-mongodb-on-macos-catalina-aab1cbe0c836

### Using/switching to another version
https://stackoverflow.com/questions/30379127/how-to-install-earlier-version-of-mongodb-with-homebrew


## Virtual Box Installation
https://www.virtualbox.org/wiki/Downloads

### Microsoft Development VM Image Download
https://developer.microsoft.com/en-us/windows/downloads/virtual-machines/

Extract the zip file and then select Import from VirtualBox

## Useful Apps

###For window resizing:
http://www.spectacleapp.com/

## Github 2-Factor Authentication for Git Cli
Set up a personal access token for accessing GitHub repositories - 
I recommend giving it gist, repo, and user scope. Make sure you copy the token now as you won't be able to later

## Using mongorestore for Mongo Data Dump
Make sure app is running `mongod`

To seed data from data dump:
```
mongorestore --db=database-name directory-with-json-bson-files
```