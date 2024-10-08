# Advanced New File

Advanced file creation for Neovim.

## Overview

The edit command in neovim does not create folders or files inside new folders.

AdvancedNewFile.nvim provides a simple and fast way to create new files and folders in the current working directory.

This plugin was inspired by [AdvancedNewFile](https://github.com/SublimeText/AdvancedNewFile) plugin in SublimeText.

It is currently tested on macOS but it should work on other operating systems.

## Installation

Install with the package installer of choice:

### vim-plug

```
Plug 'wbartz/AdvancedNewFile.nvim'
```

### Packer

```
use 'wbartz/AdvancedNewFile.nvim'
```

### Lazy

```
return {
  'wbartz/AdvancedNewFile.nvim'
}
```

## Usage

You can use `AdvancedNewFile` command to create new files and folders in neovim. You may want to map this to key bindings for easy access.

```lua
keymap("n", "<C-n>", "<cmd>lua require('advanced_new_file').run()<CR>", silent)
```

Get current file dir

```lua
keymap("n", "<C-y>", "<cmd>lua require('advanced_new_file').run(true)<CR>", silent)
```

Enter the filename in the prompt and it will be created in the current workin directory.

if the name enterd ends with a path separator, a folder will be created.

You can also create files inside new or present folders.

If installed, this plugn will work with [nvim-notify](https://github.com/rcarriga/nvim-notify).
