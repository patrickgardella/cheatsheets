---
title: i3 Window Manager
keywords: cheatsheets
last_updated: August 2, 2019
tags: [cheatsheets window_managers]
sidebar: cheatsheets_sidebar
permalink: cs_i3.html
folder: cheatsheets
---

## References

* [https://i3wm.org/docs/refcard.html](https://i3wm.org/docs/refcard.html)

Mod Key: Alt

## Change what we see

    Alt-<NUMBER>: switch to workspace NUMBER on whatever monitor it's
                attached to.
    Alt-Control-1: Only use built-in laptop display
    Alt-Control-2: Use built-in laptop display, and external display
                 positioned to its left
    Alt-<n>:    Switch to workspace <n> (need not already exist)
              (if workspace <n> is on another screen, it'll switch
              that screen to workspace <n>, not your current screen)
    Alt-<n> where <n> is the current workspace: Switch back to previous
              workspace (So you can just do Alt-1 (look at screen) Alt-1
              and be back where you started)

## Focus

    Alt-j, Alt-<left>   left
    Alt-k, Alt-<down>   down
    Alt-l, Alt-<up>     up
    Alt-;, Alt-<right>  right

## Move things

    Alt-Control-<ARROW>: Move current workspace to another monitor.
    Alt-Shift-Number: Move current window to another workspace
           (need not already exist)
    Shift-<FOCUS COMMAND>: Move current window within workspace

## Layouts

    Alt-e             default (splith/splitv), repeat to toggle
                    splith/splitv
    Alt-s             stacked
    Alt-w             tabbed
    Alt-f             fullscreen (toggle)
    Alt-S-<spc>       float  (toggle)
    Alt-mouse1-drag   move floating

    Alt-h             Make the current window/container a horizontal
                    split container. New windows opened when this
                    container is focused will be created
                    by splitting this container horizontally
                    (side-by-side)
    Alt-v             Like Alt-h, but vertical (one above another)

    Alt-e             toggle between defaulting to horizontal and
                    defaulting to vertical

## Start/end things

    Alt-return: open new terminal
    Alt-D: open dmenu at top to enter a command (output invisible,
         use to start new graphical programs)
    Alt-S-q       kill window

## Control I3

    Alt-S-c       reload I3 config
    Alt-S-r       restart I3
    Alt-S-e       kill I3 (logout)

## Resizing

    Alt-mouse2-drag  stretch or shrink window

## Screen capture

    <Printscreen> - capture whole screen
    Shift-<Printscreen> - select a rectangle or window (?)
    Control-<Printscreen> - capture currently focused window
