# NERDTree - Start and Exit

Start NERDTree. If a file is specified, move the cursor to its window.
```vim
autocmd StdinReadPre * let s:std_in=1
autocmd VimEnter * NERDTree | if argc() > 0 || exists("s:std_in") | wincmd p | endif
```

Exit Vim if NERDTree is the only window remaining in the only tab.
```vim
autocmd BufEnter * if tabpagenr('$') == 1 && winnr('$') == 1 && exists('b:NERDTree') && b:NERDTree.isTabTree() | call feedkeys(":quit\<CR>:\<BS>") | endif
```

