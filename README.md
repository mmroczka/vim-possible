# vim-possible
This repo attempts to be the most complete recreation of as many vim commands as possible – available anywhere and everywhere. This is a Karabiner elements configuration created using GokuRakuJoudo.

## What is Karabiner?

[Karabiner](https://pqrs.org/osx/karabiner/) is a powerful and stable keyboard customizer for macOS.

- You can re-map any key without any restriction. 
- You can accelerate speed of the key repeat. Karabiner offers frequently used settings. 
- You can activate them by simply clicking the checkbox in the list. If the settings which you want are not in the list, you can add them by yourself. 

Karabiner has many useful features for efficient keyboard operations. 

- You can do Emacs-style operations anywhere. 
- You can do Vi-style operations anywhere. You can do Mouse operations from keyboard.

You can do everything by modifying your keyboard!

## What is GokuRakuJoudo?

[Goku](https://github.com/yqrashawn/GokuRakuJoudo) is a tool to let you manage your Karabiner configuration with ease.

Karbiner Elements uses JSON as it's config file. This leads to thousands lines of JSON (sometimes over 20,000 lines). Which makes it really hard to edit the config file and iterate on your keymap.

Goku use the [edn format](https://github.com/edn-format/edn) to the rescue.

## What is vim-possible?

vim-possible is a configuration using GokuRakuJoudo to generate Karabiner profile, which provides – to my knowledge – the most complete set of vim commands recreated to work on any Mac.

## Vim Mode

Vim mode is the way to take full use of CapsLock key. When `CapsLock` is pressed down, vim mode will be toggled on. To get out of any mode simply press `i` for `insert` just like you would to do regular .

### Navigation Commands
#### Major Navigation Commands

| Key Combo | Effect                 |    Notes     |
|-----|------------------------|--------------|
| `h` | move left              |              |
| `j` | move down              |              |
| `k` | move up                |              |
| `l` | move right             |              |
| `w` | move one word forward  | moves you to the beginning of the next 'word' same as doing an option+right arrow then a space |
| `e` | move to word end       | moves you to the end of the current 'word' same as doing an option+right arrow |
| `b` | move one word backward |              |

#### Lesser Known Navigation Commands

| Key Combo  | Effect                 |    Notes            |
|------------|------------------------|---------------------|
| `CTRL + d` | move down 15 lines     |                     |
| `CTRL + u` | move up 15 lines       |                     |
| `CTRL + f` | move forward           | simulates page down |
| `CTRL + b` | move backward          | simulates page up   |

## Installation

1. Install [Karabiner-Elements](https://pqrs.org/osx/karabiner/)
2. Install [Goku](https://github.com/yqrashawn/GokuRakuJoudo)
3. Install k-goku

```
curl https://raw.githubusercontent.com/kchen0x/k-goku/master/karabiner.edn > ~/.config/karabiner.edn

goku
```
