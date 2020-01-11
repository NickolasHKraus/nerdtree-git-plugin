# Notes

```vim
function! NERDTreeRender()
    call nerdtree#renderView()
endfunction
```

```vim
"FUNCTION: nerdtree#renderView {{{2
function! nerdtree#renderView()
    call b:NERDTree.render()
endfunction
```

`*buffer-variable* *b:var* *b:*`
A variable name that is preceded with "b:" is local to the current buffer. Thus
you can have several "b:foo" variables, one for each buffer. This kind of
variable is deleted when the buffer is wiped out or deleted with `|:bdelete|`.

```
'render': function('260')
```

`b:NERDTree` is a dictionary.

Vimscript also supports the Javascript-style "dot" lookup when the key is a string consisting only of letters, digits and/or underscores. Try the following commands:

```vim
:echo {'a': 1, 100: 'foo',}.a
:echo {'a': 1, 100: 'foo',}.100
```

```
notation    meaning            equivalent  decimal    value(s)
-----------------------------------------------------------------------
<CR>        carriage return        CTRL-M    13       *carriage-return*
<Return>    same as <CR>                              *<Return>*
<Enter>     same as <CR>                              *<Enter>*
```
