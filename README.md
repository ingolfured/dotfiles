# dotfiles
My dotfiles for Manjaro / i3wm setup

# Inspiration
The setup comes from following [this](https://developer.atlassian.com/blog/2016/02/best-way-to-store-dotfiles-git-bare-repo/) article. We simply create a bare Git repository to store the relevant config files.

# Quick Go
From scratch we run:
```bash
git init --bare $HOME/.cfg
alias config='/usr/bin/git --git-dir=$HOME/.cfg/ --work-tree=$HOME'
config config --local status.showUntrackedFiles no
echo "alias config='/usr/bin/git --git-dir=$HOME/.cfg/ --work-tree=$HOME'" >> $HOME/.bashrc
```
and then to manage dotfiles we simply replace `git` with `config`.
