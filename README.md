
# INSTALL AND CONFIGURATION ZSH IN ARCHLINUX

#### 1. INSTALL ZSH
```sh
# for archlinux
sudo pacman -S zsh 

# for ubuntu | deb
sudo apt install zsh
```

#### 2. MAKING SET YOUR DEFAUL SHELL
```sh
chsh -s /bin/zsh

# reboot after exec command
```

#### 3. INSTALL OH MY ZSH
```sh
# Link: https://github.com/ohmyzsh/ohmyzsh
sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
```

#### 4. INSTALL PLUGINS
```sh
# reference: https://gist.github.com/n1snt/454b879b8f0b7995740ae04c5fb5b7df

# autosuggestion
git clone https://github.com/zsh-users/zsh-autosuggestions.git $ZSH_CUSTOM/plugins/zsh-autosuggestions

# syntax-highlighting)
git clone https://github.com/zsh-users/zsh-syntax-highlighting.git $ZSH_CUSTOM/plugins/zsh-syntax-highlighting

# config .zshrc
plugins=(git zsh-autosuggestions zsh-syntax-highlighting)
```

#### 5. INSTALL THEME SPACESHIP
```sh
# reference: https://spaceship-prompt.sh/getting-started/#Requirements

* git clone https://github.com/spaceship-prompt/spaceship-prompt.git "$ZSH_CUSTOM/themes/spaceship-prompt" --depth=1
* ln -s "$ZSH_CUSTOM/themes/spaceship-prompt/spaceship.zsh-theme" "$ZSH_CUSTOM/themes/spaceship.zsh-theme"

# set theme in .zshrc
ZSH_THEME="spaceship"

```
#### BONUS
```sh
# create config file
touch ~/.config/spaceship.zsh
```
* add in new file
```sh
# Display time
SPACESHIP_TIME_SHOW=true

# Display username always
SPACESHIP_USER_SHOW=always
```
* set new file in .zshrc
```sh
export SPACESHIP_CONFIG="$HOME/.config/spaceship.zsh"
```
* not display icons, add in config file
```sh
SPACESHIP_PROMPT_ASYNC=false
```
