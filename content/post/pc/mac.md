---
title: "Mac 安裝"
date: 2022-08-14T21:43:31+08:00
draft: true
---
## iTerm2
## brew
## ZSH
```bash
brew install zsh
```
## Oh My Zsh
```bash
sh -c "$(curl -fsSL https://raw.githubusercontent.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"
```

Check the installed version
```bash
zsh --version
```

Upgrade if need
```bash
omz update
```

## Powerlevel10k
```bash
git clone --depth=1 https://github.com/romkatv/powerlevel10k.git ${ZSH_CUSTOM:-$HOME/.oh-my-zsh/custom}/themes/powerlevel10k
```
Then, set `ZSH_THEME="powerlevel10k/powerlevel10k"` in `~/.zshrc`.

## pyenv

## VSCode
### Font
In `Settings`, set both `Editor` font and `Terminal` Font to 16.

### Set ZSH
In `Settings->Features->Terminal->Edit in settings.json`, add
```
"terminal.integrated.shell.osx": "/bin/zsh"
```
**Note**: The path for zsh might be different on your computer. Be sure to use the correct path.
