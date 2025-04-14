# 02 – Editing Files with Vim

In HPC environments, you’ll often find yourself needing to create or modify files directly on the cluster. While many editors exist, **Vim** is powerful and widely available — and learning just the basics will take you far.

---

## Why Vim?

- Installed by default on virtually all Unix-like systems
- Fast to use once you learn the basics
- Doesn’t require a graphical interface (perfect for remote use)

---

## Opening a File

`vim filename.inp`

## Vim Modes

Vim has **two** main modes.
| Mode | Meaning | How to Enter |
|-|-|-|
|Normal mode | Navigate, delete, copy, etc. | Press `Esc` |
| Insert mode | Type and edit text | Press `i` |

## Basic Editing Commands
| Task | Command |
|-|-|
| Enter insert mode | Press `i` |
| Exit insert mode | Press `Esc` |
| Save the file | Press `:` + `w` + `Enter` |
| Quit Vim | Press `:` + `q` + `Enter` |
| Save and quit | Press `:` + `w` + `q` + `Enter` |
| Quit without saving | `:` + `q` + `!` + `Enter` |

## Navigation Basics (Normal Mode)
| Movement | Command |
|-|-|
| Move up/down | Press `k`/`j` or `arrow UP`/`arrow DOWN` |
| Move left/right | Press `h`/`l` or `arrow UP`/`arrow DOWN` |
| Start of line | Press `0` or `Home` |
| End of Line  | Press `$` or `End` |
| Start of file | Press `:` + `1` |
| End of file | Press `SHIFT` + `G` |
| Go to a specific line | Press `:` + line_number (e.g, 25) |
| Search for text (case sensitive) | Press `/` + text |

