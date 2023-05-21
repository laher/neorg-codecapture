# neorg-capture

    **PRE-ALPHA** - breaking changes incoming soon.

Super basic capture module for neorg. I just want to capture with a line number

## Commands

`:Neorg capture popup` - opens a small popup where you enter a todo. The todo ends up in a workspace file called `inbox.norg`
`:Neorg capture inbox` - takes you to your inbox


## Config

Nah.

## 🔧 Installation

First, make sure to pull this plugin down.
This plugin does not run any code in of itself.

It requires Neorg to load it first:

You can install it through your favorite plugin manager:

-
  <details>
  <summary><a href="https://github.com/wbthomason/packer.nvim">packer.nvim</a></summary>

  ```lua
  use {
      "nvim-neorg/neorg",
      config = function()
          require('neorg').setup {
              load = {
                  ["core.defaults"] = {},
                  ...
                  ["external.capture"] = {},
              },
          }
      end,
      requires = { "nvim-lua/plenary.nvim", "laher/neorg-capture" },
  }
  ```

- <details>
  <summary><a href="https://github.com/junegunn/vim-plug">vim-plug</a></summary>

  ```vim
  Plug 'nvim-neorg/neorg' | Plug 'nvim-lua/plenary.nvim' | Plug 'laher/neorg-capture'
  ```

  You can then put this initial configuration in your `init.vim` file:

  ```vim
  lua << EOF
  require('neorg').setup {
    load = {
        ["core.defaults"] = {},
        ...
        ["external.capture"] = {},
    },
  }
  EOF
  ```

  </details>
- <details>
  <summary><a href="https://github.com/folke/lazy.nvim">lazy.nvim</a></summary>

  ```lua
  require("lazy").setup({
      {
          "nvim-neorg/neorg",
          opts = {
              load = {
                  ["core.defaults"] = {},
                  ...
                  ["external.capture"] = {},
              },
          },
          dependencies = { { "nvim-lua/plenary.nvim" }, { "laher/neorg-capture" } },
      }
  })
  ```

  </details>

