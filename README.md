# vim-printer

![](https://i.imgur.com/9ptxO4c.gif)

Quickly print/log the variable in your favourite language

## Installation

Use your favourite plugin manager to install. I use `vim-plug`.

```
Plug 'aonemd/vim-printer'
```

## Usage

There is two keybinding in each normal mode and visual mode.  In normal mode it
works on current word under cursor and in visual mode it works on the visual
selection.

- `<leader>P` to add print/log statement below current line
- `<leader>O` to add print/log statement above current line


## Configuration

You can change the default keybindings like below.  It will be used both in
normal mode and visual mode. Please note that setting a map to `''` or `' '` in
order to remove it, will result in remapping the `:` in vim which is not what
anyone wants.

```
let g:vim_printer_print_below_keybinding = '<leader>P'
let g:vim_printer_print_above_keybinding = '<leader>O'
```

You can add new languages or override existing by using:

> The text inside `{$}` will be replaced by the variable

```
let g:vim_printer_items = {
      \ 'javascript': 'console.log("{$}:", {$})',
      \ }
```

## Future TODO

- add some kind of debug mode print
    eg: `logging.log()` in python or `println!('{:?}', var)` in rust

## Alternatives

- [vim-printf](https://github.com/mptre/vim-printf)
