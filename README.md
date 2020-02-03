# NERDTree Git Plugin

This Vim plugin is a rewrite of Xuyuanp's [nerdtree-git-plugin](https://github.com/Xuyuanp/nerdtree-git-plugin).

## Installation

## Installation

### [Pathogen](https://github.com/tpope/vim-pathogen)

```bash
git clone git@github.com:NickolasHKraus/nerdtree-git-plugin.git ~/.vim/bundle/nerdtree-git-plugin
```

## [Vundle](https://github.com/VundleVim/Vundle.vim)

`.vimrc`

```vim
Plugin 'scrooloose/nerdtree'
Plugin 'NickolasHKraus/nerdtree-git-plugin'
```

```bash
vim +PluginInstall +qall
```

### [NeoBundle](https://github.com/Shougo/neobundle.vim)

`.vimrc`

```vim
NeoBundle 'scrooloose/nerdtree'
NeoBundle 'NickolasHKraus/nerdtree-git-plugin'
```

```bash
vim +NeoBundleInstall +qall
```

`NeoBundle 'scrooloose/nerdtree'`

`NeoBundle 'Xuyuanp/nerdtree-git-plugin'`

For Plug

`Plug 'scrooloose/nerdtree'`

`Plug 'Xuyuanp/nerdtree-git-plugin'`

## FAQ

> Got error message like `Error detected while processing function
177[2]..178[22]..181[7]..144[9]..142[36]..238[4]..NERDTreeGitStatusRefreshListener[2]..NERDTreeGitStatusRefresh:
line 6:
E484: Can't open file /tmp/vZEZ6gM/1` while nerdtree opening in fish, how to resolve this problem?

This was because that vim couldn't execute `system` function in `fish`. Add `set shell=sh` in your vimrc.

This issue has been fixed.

> How to config custom symbols?

Use this variable to change symbols.

```vimscript
let g:NERDTreeIndicatorMapCustom = {
    \ "Modified"  : "✹",
    \ "Staged"    : "✚",
    \ "Untracked" : "✭",
    \ "Renamed"   : "➜",
    \ "Unmerged"  : "═",
    \ "Deleted"   : "✖",
    \ "Dirty"     : "✗",
    \ "Clean"     : "✔︎",
    \ 'Ignored'   : '☒',
    \ "Unknown"   : "?"
    \ }
```

> How to show `ignored` status?

`let g:NERDTreeShowIgnoredStatus = 1` (a heavy feature may cost much more time)

## Credits

*  [scrooloose](https://github.com/scrooloose): Open API for me.
*  [git_nerd](https://github.com/swerner/git_nerd): Where my idea comes from.
*  [PickRelated](https://github.com/PickRelated): Add custom indicators & Review code.
