# My Neovim Configuration

This is a personalized Neovim configuration based on [LazyVim](https://www.lazyvim.org/).

## Core Configuration

### `init.lua`

The main entry point of the configuration. It simply bootstraps `lazy.nvim` by loading the `lazy.lua` file.

### `lua/config/lazy.lua`

This file configures `lazy.nvim`, the plugin manager. It specifies the plugin spec, which includes LazyVim's plugins and custom plugins from the `plugins` directory. It also sets default plugin loading behavior and other performance-related settings.

### `lua/config/options.lua`

This file is intended for setting general Neovim options.

### `lua/config/keymaps.lua`

This file is for defining custom keymaps.

### `lua/config/autocmds.lua`

This file contains autocommands. Currently, it sets the `guicursor` to be empty and disables `relativenumber` in favor of `number`.

## Plugins

### `lua/plugins/autosave.lua`

- **Plugin:** `Pocco81/auto-save.nvim`
- **Functionality:** Automatically saves files on the `InsertLeave` event.

### `lua/plugins/completion.lua`

- **Plugin:** `hrsh7th/nvim-cmp`
- **Dependencies:** `supermaven-nvim`
- **Functionality:** Configures code completion. It integrates `supermaven` as a completion source and sets up custom keymappings for navigating the completion menu with `<Tab>` and `<S-Tab>`. It also customizes the appearance of the completion and documentation windows.

### `lua/plugins/dashboard.lua`

- **Plugin:** `nvimdev/dashboard-nvim`
- **Functionality:** Provides a custom startup dashboard with a personalized logo and a menu of common actions like finding files, creating new files, and accessing recent files.

### `lua/plugins/disabled.lua`

- **Disabled Plugins:**
  - `folke/persistence.nvim`

### `lua/plugins/flutter.lua`

- **Plugins:**
  - `akinsho/flutter-tools.nvim`
  - `dart-lang/dart-vim-plugin`
- **Functionality:** Configures the environment for Flutter development. It sets the path to the Flutter SDK, customizes the UI for Flutter tools, and configures the debugger and LSP settings for Dart.

### `lua/plugins/git.lua`

- **Plugin:** `lewis6991/gitsigns.nvim`
- **Functionality:** Provides Git integration in the editor. It adds custom keymappings for navigating between Git hunks.

### `lua/plugins/harpoon.lua`

- **Plugin:** `ThePrimeagen/harpoon`
- **Functionality:** Adds the Harpoon plugin for quick file navigation.

### `lua/plugins/lsp-inlayhints.lua`

- **Plugin:** `neovim/nvim-lspconfig`
- **Functionality:** Disables inlay hints for the LSP client.

### `lua/plugins/snippet.lua`

- **Plugin:** `L3MON4D3/LuaSnip`
- **Functionality:** Configures snippets for different filetypes, extending `dart` with `flutter` and `javascript` with `javascriptreact` and `html`.

### `lua/plugins/themes.lua`

- **Configured Themes:**
  - `sainnhe/everforest`
  - `catppuccin/nvim` (mocha flavor)
  - `folke/tokyonight.nvim` (transparent background)
  - `rebelot/kanagawa.nvim`
  - `EdenEast/nightfox.nvim`
- **Default Colorscheme:** `tokyonight`

### `lua/plugins/ui.lua`

- **Plugin:** `snacks.nvim`
- **Functionality:** Customizes the UI by disabling indent lines and the scope indicator.

### `lua/plugins/which-key.lua`

- **Plugin:** `folke/which-key.nvim`
- **Functionality:** Configures `which-key` to display a description for the `<leader>q` keymap.
