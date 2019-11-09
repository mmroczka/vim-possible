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

| Key Symbol |   Keyboard Button    | Note                       |
|------------|----------------------|----------------------------|
| `⌥`        |       option         |                            |
| `⌘`        |       command        |                            |
| ⇧          |       shift          | Note the difference between shift (⇧) and the up arrow (↑) on a keyboard |
| ⌃          |       control        |                            |
| ⇪          |       capslock       |                            |

### Cursor Movement Commands
| Key Combo | Effect                         |  Keyboard Equivalent   |
|-----------|--------------------------------|------------------------|
| `k`       | moves cursor up                |      `↑`               |
| `j`       | moves cursor down              |      `↓`               |
| `h`       | moves cursor left              |      `←`               |
| `l`       | moves cursor right             |      `→`               |
| `w`       | moves cursor one word forward  |      `⌥`+`→`, `→`      |
| `e`       | move to word end               |      `⌥`+`→`           |
| `b`       | move one word backward         |      `⌥`+`←`           |
| `gg`      | go to top of file              |      `⌘`+`↑`           |
| ⇧+`g` or `G` | go to bottom of file        |      `⌘`+`↓`           |
| ⇧+`5` or `%` | :no_entry_sign: Not possible. Need context we don't have.  |
| ⇧+`w` or `W` | :no_entry_sign: Not possible. Need context we don't have.  |
| ⇧+`e` or `E` | :no_entry_sign: Not possible. Need context we don't have.  |
| ⇧+`b` or `B` | :no_entry_sign: Not possible. Need context we don't have.  |
| ⇧+`h` or `H` | :construction: TODO: should move to top of screen. research if possible. :warning:    |
| ⇧+`m` or `M` | :construction: TODO: should move to middle of the screen. research if possible. :warning: |
| ⇧+`l` or `L` | :construction: TODO: should move to bottom of screen. research if possible. :warning:     |
| ⇧+`4` or `$` | move to start of line       |      `⌘`+`←`           |
| `0`       | move to end of line            |      `⌘`+`→`           |
| ⌃+`d`     | move down 15 lines             | `↓` but like pressed 15 times |
| ⌃+`u`     | move up 15 lines               | `↑` but like pressed 15 times |
| ⌃+`f`     | move forward                   |      page down         |
| ⌃+`b`     | move backward                  |      page up           |

### Insert Commands
| Key Combo | Effect                       |   Mode Change   |    Keyboard Equivalent     |
|-----------|------------------------------|-----------------|----------------------------|
| `i`       |                              | toggles off `vim mode` to `insert mode` |    |
| ⇧+`i`     | move to beginning of line    | `vim mode` to `insert mode` |     `⌘`+`←`    |
| `a`       | move cursor right            | `vim mode` to `insert mode` |                |
| ⇧+`a`     | move to end of line          | `vim mode` to `insert mode` |     `⌘`+`→`    |
| `ea`      | :construction: TODO: insert (append) at the end of the word | `vim mode` to `insert mode` |   `⌥`+`→`   |
| `o`       | append (open) new line below current line | `vim mode` to `insert mode` | `⌘`+`→`, `return`  |
| ⇧+`o`     | append (open) new line above current line | `vim mode` to `insert mode` | `↑`, `⌘`+`→`, `return` |



#### Editing Commands
| Key Combo  | Effect                         |   Mode Change   |    Keyboard Equivalent     |
|------------|--------------------------------|-----------------|----------------------------|
| `r`<char to replace> | replace a single character |           | `delete_forward` + `<char>`|
| ⇧+`j` or `J` | join line below to the current one |           |  `⌘`+`→`, `delete_forward` |
| `cc`        | change (replace) entire line  | `vim mode` to `insert mode` | `⌘`+`←`, ⇧+`⌘`+`→`, `delete` |
| `C`         |  change (replace) to the end of the line  | `vim mode` to `insert mode` | ⇧+`⌘`+`→`, `delete` |
| `c`+`⇧+`4` or `c$` |  change (replace) to the end of the line  | `vim mode` to `insert mode` | ⇧+`⌘`+`→`, `delete` |
| `ciw`       | change (replace) entire word | `vim mode` to `insert mode` | `⌥`+`←`, ⇧+`⌥`+`→`, `delete` |
| `cw`        | change (replace) to the end of the word | `vim mode` to `insert mode` | `⌥`+`→`, `delete` |
| `s`         | delete character and substitute text | `vim mode` to `insert mode` | `delete_forward` |
| `S`         | delete line and substitute text (same as cc) | `vim mode` to `insert mode` | `⌘`+`←`, ⇧+`⌘`+`→`, `delete` |
| `xp`        | transpose two letters (delete and paste)     | `vim mode` to `insert mode` | ⇧+`→`, `⌘`+`c`, `delete`, `→`, `⌘`+`v` |
| `u`        | undo last action       |                     |                                |
| `⌃`+`r`    | redo last action       |                     |                                |
  
## Installation

1. Install [Karabiner-Elements](https://pqrs.org/osx/karabiner/)
2. Install [Goku](https://github.com/yqrashawn/GokuRakuJoudo)
3. Install vim-possible

```
curl https://.../master/karabiner.edn > ~/.config/karabiner.edn

goku
```
