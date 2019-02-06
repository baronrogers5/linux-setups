# Installation Instructions for fresh zsh and pure prompt installation

## Things that will be installed

1. zsh
2. oh-my-zsh
3. Installing npm
4. pure prompt
5. zsh-syntax highlighting
6. consolas font
7. Terminal colors and settings 


## Installing zsh

```shell
sudo apt -y install zsh
```

## Installing oh-my-zsh
```shell
sh -c "$(wget https://raw.github.com/robbyrussell/oh-my-zsh/master/tools/install.sh -O -)"
```
## Installing npm
```shell
sudo apt -y install npm
```

## Installing pure prompt
```shell
sudo npm install --global pure-prompt --allow-root --unsafe-perm=true
```
 > Set ZSH_THEME="" in your ~/.zshrc to disable oh-my-zsh themes.
 
In .zshrc, after ZSH_THEME,
> autoload -U promptinit; promptinit

NOTE: oh-my-zsh overrides the prompt so Pure must be activated after source $ZSH/oh-my-zsh.sh
> prompt pure
at the very end of the file

## Install zsh-syntax-highlighting
```shell 
cd ~/.ohmyzsh/plugins

git clone https://github.com/zsh-users/zsh-syntax-highlighting.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-syntax-highlighting
```
In ~/.zshrc
> plugins=( [plugins...] zsh-syntax-highlighting)


## Download consolas font (only on linux, not required on windows)
> https://github.com/kakkoyun/linux.files/raw/master/fonts/Consolas.ttf


## Import gnome-terminal profile (applicable only for gnome-terminal)
```shell
dconf load /org/gnome/terminal/legacy/profiles:/ < gnome-terminal-profiles.dconf
```
