---
title: zsh
date: 2020-08-31 10:28:36
tags:
---

# zsh 笔记

## 安装

一说 `zsh` 就离不开 `oh-my-zsh`, 别问为啥，装就对了

```bash
# https://ohmyz.sh/#install
sh -c "$(curl -fsSL https://raw.github.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
```

## 插件

```bash
# cd ~/.oh-my-zsh/plugins
git clone https://github.com/zsh-users/zsh-autosuggestions.git
git clone https://github.com/zsh-users/zsh-syntax-highlighting.git
# vim ~/.zshrc
plugins=(git vscode zsh-autosuggestions zsh-syntax-highlighting)

source ~/.zshrc
```