# Installation Instructions for fresh zsh and pure prompt installation

## Things that will be installed

1. zsh
2. oh-my-zsh
3. pure prompt
4. zsh-syntax highlighting
5. consolas font
6. Terminal colors and settings 


## Installing zsh

```shell
sudo apt install zsh
```

## Installing oh-my-zsh
```shell
sh -c "$(wget https://raw.github.com/robbyrussell/oh-my-zsh/master/tools/install.sh -O -)"
```

## Installing pure prompt
```shell
sudo npm install --global pure-prompt --allow-root --unsafe-perm=true
```
 > Set ZSH_THEME="" in your .zshrc to disable oh-my-zsh themes.
 
In .zshrc
> autoload -U promptinit; promptinit

NOTE: oh-my-zsh overrides the prompt so Pure must be activated after source $ZSH/oh-my-zsh.sh
> prompt pure

## Install zsh-syntax-highlighting
```shell 
cd ~/.ohmyzsh/plugins

git clone https://github.com/zsh-users/zsh-syntax-highlighting.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-syntax-highlighting
```
In ~/.zshrc
> plugins=( [plugins...] zsh-syntax-highlighting)


## Download consolas font
> https://github.com/kakkoyun/linux.files/raw/master/fonts/Consolas.ttf


## Import gnome-terminal profile
```shell
dconf load /org/gnome/terminal/legacy/profiles:/ < gnome-terminal-profiles.dconf
```
