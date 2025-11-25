---
title: "Neovim: A code editor for nerds"
description: "I learnt Neovim as a side quest and so here's a brief overview~"
slug: neovim-guide
date: 2025-11-25T15:58:10.246Z
lastMod: 2025-11-25T15:58:10.479Z
authors:
    - Andreaa
image: cover.jpg
categories:
    - guide
tags:
    - coding
---

# Introduction

If you're a developer, without a doubt you've heard of at least a few Integrated Development Environments (or IDEs for short), with the most common ones being Pycharm or Visual Studio Code (not to be confused with Visual Studio, thanks Microsoft for the totally not confusing naming schemes). But, unless you're like a total nerd, what you probably haven't heard of is: Neovim!

## So, What's Neovim & why use it?

Neovim is a terminal-based text editor that focuses on efficient editing with the keyboard. The power in this may not be obvious, especially considering how universal the mouse is. Why would anyone want to use just their keyboard? Isn't that just voluntarily handicapping yourself? Well, not so! In fact, the motions that you're able to do with vim motions are incredibly powerful: allowing you to do nearly anything with just a few keystrokes. There's the obvious things you'd expect with a text editor like moving around (but conveniently using just the home row), or inserting text, or selecting and deleting text. But, there's so much more, like deleting whole words or whole lines, replacing text in brackets, and with certain plugins even replacing the contents of a function. I'll cover the actual bindings in a later section.

Now, for the code editing part: why in the world did I compare a text editor to IDEs? Well, Neovim is highly extensible and allows for the installation of plugins. This allows it to functionally become an IDE with enough configuration. The core way to do this is by fully building a configuration yourself from scratch in the configuration files, but for obvious reasons this is very daunting. Luckily though, there are many different things that help set Neovim up for you, from the simplest `kickstart.nvim` which just gives you a base configuration file to start with, to LunarVim which gives you a fully-featured IDE from the get-go. Personally, I used LazyVim because that's what my friend recommended me (and she's a total nerd so I trust her). It lies in-between the bare minimum and a full setup, giving you some useful plugins and additional tools that you can install should you want to.

## How 2 Neovim (not really)

> [!NOTE]
> This isn't really a guide but more of me just showcasing some of the things that you can do in Neovim, if you try to use this as a learning resource you might want to cry :3

I'll preface by saying that learning Vim keybindings is not intuitive whatsoever, and relies on you to put in the effort to do so. That's not to say that they're *nonsensical*, just that it doesn't come naturally. I'd recommend using the `:Tutor` command in Neovim to learn the basics (or watch one of many helpful youtube videos). `:help` is also a nice command, allowing you to get a reference for any command or binding using `:help [command you need help with]`.

Something important about (Neo)vim is that it is a modal text editor. This means that for example, there's a mode for navigation and actions (Normal Mode), insertion of text (Insert Mode), and selection of text (Visual Mode). This is what trips people up the most in the beginning I feel, even more so than the weird keybindings. Learning to type `:q` isn't the issue in quitting, often I find it's accidentally entering insert mode, not even realising, and fruitlessly trying to quit from there. In conventional editors, there's just one mode: editing. You use your mouse to navigate and select (usually), and your keyboard for inserting text, and that's it. The major downside to this is constantly having to navigate back and forth the keyboard and mouse, which can feel tedious and can bring you out of the flow state... Or maybe that's just a nerd problem. But either way, things will get much smoother once you start learning how to enter the correct mode to do things.

Now, for the important part, bindings! Now, who could neglect the beloved `hjkl` to navigate? `h` for left, `j` for down, `k` for up, and `l` for right.their presence on the home row is so much nicer ergonomically speaking, compared to having to move my hands down in order to navigate. Other essential actions would be using `i` to enter insert mode to actually edit your file, and `Esc` to go back to normal mode once you're done. Another important keybind is `:` in normal mode, which enters command mode and where if you're sick of Neovim already you can then do `quit` (`q` for short) to quit. (For ease of reading I'll use `:` in front of command mode commands from here onwards. If you've made changes, you can use `:write` (`:w` for short), or you can chain certain commands like `:wq` to write then quit the window to make life easier.

For the more powerful bindings, they usually come in sets of keys; what I've referred to as keybindings are actually called *vim motions*. Using vim motions, you can do `dd` to delete a line, or `diw` to delete a word. These may seem illogical at first but there's a method to the madness -- what a key like `d` is is an *operator*. It waits for you to define a target, like `d` again to delete the line or `iw` to delete *in (the) word* that you are currently on.

To be totally honest, the keybinds are kinda jank, but they try their best to make at least some sort of sense. For example, where `x` is an arbitary operator, `xx` generally operates on a line. `yy` yanks/copies a line like how `dd` deletes a line. Attempts for more sane defaults in new vim-inspired editors like Helix or Kakoune have been attempted, but regardless Vim bindings live on as the default.

## Conclusion

In my opinion, what's most important is that you stick to what you like the best and works the best for you. If you have a system set up already with whatever you're using, it's best to just stick with that. But if you feel limited by your current setup, and you have that itch for extra efficiency, extra flow, extra power, then you may want to consider new options like Neovim. And if you do indeed swap over, its equally as important to then stick with your current configuration once it's good enough, instead of endlessly messing about with it; go get some work done with your fancy new tool! Only once the grievances build up past a boiling point, only then should you refactor everything all at once, it saves lotsss of trouble.

And as with learning new things, your brain can only learn so much at once, so just learn one or two new motions, and eventually you'll know lots of powerful motions! So, go out there and have some fun~

(Note: I wrote this fully in Neovim btw~)

## Resources

- `:Tutor` mode
- [LazyVim Documentation](https://www.lazyvim.org)  
- [Video on Vim Motions](https://www.youtube.com/watch?v=z4eA2eC28qg)
