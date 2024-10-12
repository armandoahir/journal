---
title: 'Friday Night Ricing'
date: 2024-10-12
permalink: /_posts/2024/
tags:
 - Linux
---

![](percorso/della/rice.jpg)


This Friday night, I decided to set up Neovim to make it more programming-oriented. I started by cloning the recommended repository for customization: ["nvim-lua/kickstart.nvim"](https://github.com/nvim-lua/kickstart.nvim).

This repository encouraged me to do everything in Lua, so I spent about 30-60 minutes getting familiar with the language. I aimed to promote modular programming, focusing on future reuse.

The goal is to organize Neovim like any modern programming environment while keeping the Vim commands (Vim motions).

### Added Features

Here are some of the features I implemented:

- Added a theme sourced from GitHub.

To incorporate a transparency toggle, I used the following code:

'''javascript
local toggle_transparency = function()
    bg_transparent = not bg_transparent
    vim.g.nord_disable_background = bg_transparent
    vim.cmd [[colorscheme nord]]
end
vim.keymap.set('n', '<leader>bg', toggle_transparency, {noremap = true, silent = true})


### Folder Organization

The nvim folder contains two subfolders: core and plugins.

    Core Folder: This contains my personalized key mappings to enhance navigation ergonomics within the environment. Additionally, the core folder has an options.lua file, which is a standard IDE configuration inspired by an online Neovim setup.

    Plugins Folder: This houses Lua scripts for:

        Autocompletion: Provides suggestions for code completion as you type, improving coding efficiency. It's disabled when not programming.

        Bufferline: Displays open buffers as tabs at the top of the Neovim window, making navigation between files easier.

        Color Theme: Allows for customization of Neovim's appearance, enhancing visual aesthetics.

        Comment: Adds functionality for easily commenting and uncommenting lines of code.

        Indent Blankline: Displays indentation guides, helping to visualize the structure of the code.

        LSP (Language Server Protocol): Integrates language servers to provide features like autocompletion, error checking, and code navigation.

        Neo-tree: A file explorer plugin that provides a tree view of your files, making it easy to navigate your project.

        Telescope: A powerful fuzzy finder for Neovim that allows you to search through files, buffers, and more efficiently.

        Treesitter: A syntax highlighting and code parsing library that enhances code understanding and navigation.
