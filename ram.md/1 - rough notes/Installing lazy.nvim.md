14-12-2024 18:58:47

Tags : [[nvim]] [[lazy.nvim]] [[Lua]]

```lua
-- ~/.config/nvim/init.lua
require("config.lazy")
```

You may think to you need to create config.lazy.lua file - no
0r config/lazy.lua - almost!

- Neovim only looks into lua files to require inside of folder that have lua/ as top level folder
- This lua folder must be in the runtime path.

```vimrc
:echo nvim_list_runtime_paths()
```

So therefore we have to create a lua folder in our config directory

```vimrc
:!mkdir lua/config
```

Create ~/.config/nvim/lua/config/lazy.lua 

```vimrc
:e lua/config/lazy.lua
```

```lua
-- Bootstrap lazy.nvim
local lazypath = vim.fn.stdpath("data") .. "/lazy/lazy.nvim"
if not (vim.uv or vim.loop).fs_stat(lazypath) then
  local lazyrepo = "https://github.com/folke/lazy.nvim.git"
  local out = vim.fn.system({ "git", "clone", "--filter=blob:none", "--branch=stable", lazyrepo, lazypath })
  if vim.v.shell_error ~= 0 then
    vim.api.nvim_echo({
      { "Failed to clone lazy.nvim:\n", "ErrorMsg" },
      { out, "WarningMsg" },
      { "\nPress any key to exit..." },
    }, true, {})
    vim.fn.getchar()
    os.exit(1)
  end
end
vim.opt.rtp:prepend(lazypath)

-- Make sure to setup `mapleader` and `maplocalleader` before
-- loading lazy.nvim so that mappings are correct.
-- This is also a good place to setup other settings (vim.opt)
vim.g.mapleader = " "
vim.g.maplocalleader = "\\"

-- Setup lazy.nvim
require("lazy").setup({
  spec = {
    -- import your plugins
    { import = "plugins" },
  },
  -- Configure any other settings here. See the documentation for more details.
  -- colorscheme that will be used when installing plugins.
  install = { colorscheme = { "habamax" } },
  -- automatically check for plugin updates
  checker = { enabled = true },
})
```

## References

[lazy.nvim][https://lazy.folke.io/installation]
[lazy.nvim explained - TJ DeVries][https://youtu.be/_kPg0VBRxJc?si=KUky-e6EbwBV-gem]