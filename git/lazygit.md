# git - Lazygit

https://github.com/jesseduffield/lazygit

> simple terminal UI for git commands

##  Open lazygit via shortcut within a fullscreen popup

```vim
function! FloatingLazygit()
    let buf = term_start('lazygit', {'hidden': 1, 'term_finish': 'close'})
    let opts = {
        \ 'line': 1,
        \ 'col': 1,
        \ 'minwidth': &columns - 2,
        \ 'minheight': &lines - 4,
        \ 'maxwidth': &columns - 2,
        \ 'maxheight': &lines - 4,
        \ 'zindex': 300,
        \ 'border': [],
        \ }
    call popup_create(buf, opts)
    startinsert
endfunction

nnoremap <leader>g :call FloatingLazygit()<CR>
```

