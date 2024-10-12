---
title: 'Friday night ricing'
date: 2024-10-12
permalink: /posts/2024/10/blog-post/
#tags:
 - Linux
---

Per questo venerdì sera ho pensato di sistemare Vim, rendendolo più orientato alla programmazione.
Sono partito clonando la repository consigliata per iniziare la personalizzazione ["nvim-lua/kickstart.nvim"].
La repository mi ha spinto a fare tutto in Lua e quindi ho speso 30-60 minuti a prendere confidenza con il linguaggio.
Ho voluto favorire la programmazione modulare, orientandola ad un riuso futuro

Il fine è quello di organizzare vim come SublimeText, mantenendo i comandi vim motions.
Le funzionalità aggiunte sono state:
- Aggiunta di un tema preso su github.

Ecco il codice per aggiungere lo switch di trasparenza:

    local toggle_transparency = function()
        bg_transparent = not bg_transparent
        vim.g.nord_disable_background = bg_transparent
        vim.cmd [[colorscheme nord]]
        end
        vim.keymap.set('n', '<leader>bg', toggle_transparency, {noremap = true, silent = true})
    end


