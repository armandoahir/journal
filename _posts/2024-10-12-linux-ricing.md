---
title: 'Friday Night Vim Ricing'
date: 2024-10-12
permalink: /friday-night-ricing
tags:
 - Linux   
---

<p align="center">
    <img src = "https://github.com/user-attachments/assets/0b5913f3-713e-4ecc-92c5-c0835234dceb"/>
</p>

This Friday night, I decided to set up Neovim to make it more programming-oriented. I started by cloning the recommended repository for customization: [nvim-lua kickstart](https://github.com/nvim-lua/kickstart.nvim).

This repository encouraged me to do everything in Lua, so I spent about 30-60 minutes [getting familiar with the language](https://learnxinyminutes.com/docs/lua/). I aimed to promote modular programming, focusing on future reuse.

The goal is to organize Neovim like any modern programming environment while keeping Vim concepts alive.

### Added Features


To incorporate a transparency toggle, I used the following code:

    local toggle_transparency = function()
        bg_transparent = not bg_transparent
        vim.g.nord_disable_background = bg_transparent
        vim.cmd [[colorscheme nord]]
    end
    vim.keymap.set('n', '<leader>bg', toggle_transparency, {noremap = true, silent = true})


### Folders Organization

The nvim folder contains two subfolders: **core** and **plugins**.

**Core Folder**: This contains my personalized key mappings to enhance navigation ergonomics within the environment. Additionally, the core folder has an options.lua file, which is a standard IDE configuration inspired by an online Neovim setup.

**Plugins Folder**: This houses Lua scripts for:

<p align="center">
    <img src = "https://github.com/user-attachments/assets/3eff5553-a305-4066-98ac-3c3ab0fee9e4"/>
</p>

- **[Autocompletion](https://github.com/L3MON4D3/LuaSnip.git)**: Provides suggestions for code completion as you type, improving coding efficiency. It's disabled when not programming.

- **[Bufferline](https://github.com/nvim-tree/nvim-web-devicons.git)**: Displays open buffers as tabs at the top of the Neovim window, making navigation between files easier.

- **Color Theme**: Allows for customization of Neovim's appearance, enhancing visual aesthetics.

- **[Comment](https://github.com/numToStr/Comment.nvim.git)**: Adds functionality for easily commenting and uncommenting lines of code.
 
- **[Indent Blankline](https://github.com/lukas-reineke/indent-blankline.nvim.git)**: Displays indentation guides, helping to visualize the structure of the code.

- **[LSP (Language Server Protocol)](https://github.com/williamboman/mason.nvim.git)**: Integrates language servers to provide features like autocompletion, error checking, and code navigation.

- **[Neo-tree](https://github.com/nvim-neo-tree/neo-tree.nvim.git)**: A file explorer plugin that provides a tree view of your files, making it easy to navigate your project.

- **[Telescope](https://github.com/nvim-telescope/telescope.nvim.git)**: A powerful fuzzy finder for Neovim that allows you to search through files, buffers, and more efficiently.

- **[Treesitter](https://github.com/tree-sitter/tree-sitter.git)**: A syntax highlighting and code parsing library that enhances code understanding and navigation.

<p align="center">
    <img src = "https://github.com/user-attachments/assets/2b99136d-1765-41a9-a60b-0e9a38699f60"/>
</p>

