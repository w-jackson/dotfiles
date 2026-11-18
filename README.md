# dotfiles

A place for my shared config managed with [GNU Stow](https://www.gnu.org/software/stow).

## Usage

Each app gets it's own package folder.

```text
zsh -> ~/dotfiles/zsh
git -> ~/dotfiles/git
...
```

The package folder for an app should mirror the struture it's config would normally take in the home dir. This means making a `.config/<app-name>` folder in some cases.

```text
~/.zshrc -> ~/dotfiles/zsh/.zshrc
~/.gitconfig -> ~/dotfiles/git/.gitconfig
~/.config/git/ignore -> ~/dotfiles/git/.config/git/ignore
...
```

To update the symlink for a single app (from `~/dotfiles`):

```bash 
stow <app-name>
```

To update all symlinks (from `~/dotfiles`):

```bash
stow */
```

