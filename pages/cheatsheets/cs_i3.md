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

Mod Key: <kbd>Alt</kbd> ⌥ (Mod1)

## Focus

    Alt-j or Alt-<left>   left
    Alt-k or Alt-<down>   down
    Alt-l or Alt-<up>     up
    Alt-; or Alt-<right>  right
    Alt-space  		toggle focus mode

## Workspace

    Alt-<n>:    Switch to workspace <n> (need not already exist)
                (if workspace <n> is on another screen, it'll switch
                that screen to workspace <n>, not your current screen)
    Alt-Shift-Number: Move current window to another workspace
           (need not already exist)
    Shift-<FOCUS COMMAND>: Move current window within workspace

    Alt-Control-1: Only use built-in laptop display
    Alt-Control-2: Use built-in laptop display, and external display
                   positioned to its left

    Alt-Control-<ARROW>: Move current workspace to another monitor.

## Layouts

    Alt-e             toggle between defaulting to horizontal and
                      defaulting to vertical
    Alt-s             stacked
    Alt-w             tabbed

## Resize Window

    Alt-f             fullscreen (toggle)
    Alt-r             resize mode
    Alt-h             Make the current window/container a horizontal
                      split container. New windows opened when this
                      container is focused will be created
                      by splitting this container horizontally
                      (side-by-side)
    Alt-v             Like Alt-h, but vertical (one above another)
    Alt-mouse2-drag   stretch or shrink window

## Floating

    Alt-Shift-<spc>   float  (toggle)
    Alt-mouse1-drag   move floating

## Start/end things

    Alt-return:       open new terminal
    Alt-d:            open dmenu at top to enter a command (output invisible,
                      use to start new graphical programs)
    Alt-Shift-q       kill window

## Control I3

    Alt-Shift-c       reload I3 config
    Alt-Shift-r       restart I3
    Alt-Shift-e       kill I3 (logout)

## Screen capture

    <Printscreen> - capture whole screen
    Shift-<Printscreen> - select a rectangle or window (?)
    Control-<Printscreen> - capture currently focused window
