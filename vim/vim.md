# Vim Cheat Sheet: Movement & Actions

## 🧭 Basic Movement
| Key           | Action                         |
|---------------|--------------------------------|
| `h`           | Left                           |
| `l`           | Right                          |
| `j`           | Down                           |
| `k`           | Up                             |
| `0`           | Beginning of line              |
| `^`           | First non-blank character      |
| `$`           | End of line                    |
| `w`           | Next word                      |
| `W`           | Next WORD (space delimited)    |
| `b`           | Back one word                  |
| `B`           | Back one WORD                  |
| `e`           | End of word                    |
| `G`           | Go to bottom                   |
| `gg`          | Go to top                      |
| `H`           | Top of screen                  |
| `M`           | Middle of screen               |
| `L`           | Bottom of screen               |
| `Ctrl-d`      | Half-page down                 |
| `Ctrl-u`      | Half-page up                   |
| `Ctrl-f`      | Full-page forward              |
| `Ctrl-b`      | Full-page backward             |
| `zz`          | Center cursor line on screen   |

---

## 🔨 Actions
| Key           | Action                         |
|---------------|--------------------------------|
| `i`           | Insert before cursor           |
| `I`           | Insert at line start           |
| `a`           | Append after cursor            |
| `A`           | Append at line end             |
| `o`           | Open new line below            |
| `O`           | Open new line above            |
| `x`           | Delete character under cursor  |
| `X`           | Delete character before cursor |
| `dd`          | Delete (cut) line              |
| `yy`          | Yank (copy) line               |
| `p`           | Paste below                    |
| `P`           | Paste above                    |
| `u`           | Undo                           |
| `Ctrl-r`      | Redo                           |
| `.`           | Repeat last change             |

---

## 🔍 Searching
| Key           | Action                         |
|---------------|--------------------------------|
| `/pattern`    | Search forward                 |
| `?pattern`    | Search backward                |
| `n`           | Next match                     |
| `N`           | Previous match                 |
| `*`           | Search word under cursor (fwd) |
| `#`           | Search word under cursor (bwd) |

---

## 🔧 Visual Mode
| Key           | Action                         |
|---------------|--------------------------------|
| `v`           | Start visual mode (char)       |
| `V`           | Visual line mode               |
| `Ctrl-v`      | Visual block mode              |
| `y`           | Yank selected text             |
| `d`           | Delete selected text           |
| `>` / `<`     | Indent left/right              |

---

## 🧠 Misc
| Key           | Action                         |
|---------------|--------------------------------|
| `:w`          | Save                           |
| `:q`          | Quit                           |
| `:wq` / `ZZ`  | Save and quit                  |
| `:q!`         | Force quit without saving      |
| `:e filename` | Open file                      |
| `:set nu`     | Show line numbers              |

---

## 🏁 Insert Mode Shortcuts
| Key           | Action                         |
|---------------|--------------------------------|
| `Esc`         | Exit insert mode               |
| `Ctrl-h`      | Delete char before cursor      |
| `Ctrl-w`      | Delete word before cursor      |
| `Ctrl-u`      | Delete to beginning of line    |