The intention of this repository is to document my journey learning Vim.

I'll use Neovim and LazyVim to easy up the path, but this might change.

First things first, we need to make sure that we have all installed in our system in order to begin.

## Install Neovim
Choose your prefered method in the official Neovim Wiki: https://github.com/neovim/neovim/wiki/Installing-Neovim

## Install LazyVim
LazyVim comes with a set of plugins and configs that makes the use of Neovim more easy, just follow the instructions on https://www.lazyvim.org/ and we are good to go!

### colorscheme (optional)
I don't like the default colorscheme from LazyVim, I like [AstroTheme](https://github.com/AstroNvim/astrotheme), so, in order to install and use it, just paste the following lines into `~/.config/nvim/lua/plugins/astrotheme.lua`
```lua
return {
  {
    "AstroNvim/astrotheme",
    lazy = false,
    priority = 1000,
    config = function()
      require("astrotheme").setup()
      vim.cmd([[colorscheme astrodark]])
    end,
  },
}
```
### intelephense (php LSP)
put the following lines into `~/.config/nvim/lua/plugins/lsp.lua`
```lua
return {
  {
    "neovim/nvim-lspconfig",
    ---@class PluginLspOpts
    opts = {
      autoformat = false,
      servers = {
        intelephense = {
          settings = {
            intelephense = {
              format = {
                braces = "k&r",
              },
            },
          },
        },
      },
    }
  }
}
```
## ...and the Journey begins!
This repo will be organised using folders, but this might change :)

## Let's go!
