# KALE - Keegan's Awful Lite Editor

I love **Nano/Micro**, I wanted to love **NeoVim**, but couldn't — so I made my own text editor called **K.A.L.E.**, or _Keegan's Awful Lite Editor_.
Am I now realising I could've played with config files in NeoVim? Yes.
Am I now too committed to this project to switch and admit I'm wrong? Also yes.

📫 **Contact**: [cautiousdollop@protonmail.com](mailto:cautiousdollop@protonmail.com)

---

## ⚠️ Current State

**Massively unfinished**, but surprisingly functional. Has some degree of syntax highlighting for quite a few languages.

KALE is **Open Source**, but I'm not really in a position to accept contributions to the code at the moment. This is a small project I work on when I feel like it.

---

## 🛠️ Installation Instructions (Linux, currently no Mac or Windows instructions)

```bash
# Move the script and make it executable
mv kale.py kale
chmod +x kale

# Install system-wide (requires sudo)
sudo mv kale /usr/local/bin/kale

# OR install for single user
mkdir -p ~/.local/bin
mv kale ~/.local/bin/kale
export PATH="$HOME/.local/bin:$PATH"
source ~/.bashrc

# Test it
kale test.txt
```

---

## 📘 Controls & Keybindings

KALE operates in **two main modes**:

- `COMMAND` mode — for navigation and editor controls
- `WRITE` mode — for editing text

Switch modes using the **Spacebar** and **Escape**.

---

### 🧭 General Controls (Both Modes)

| Key           | Action                            |
|---------------|-----------------------------------|
| `Spacebar`    | Switch to WRITE mode              |
| `ESC`         | Switch to COMMAND mode / Cancel   |
| `Ctrl+S`      | Save                              |
| `Ctrl+Q`      | Quit                              |
| `Ctrl+Z`      | Undo                              |
| `Ctrl+Y`      | Redo                              |
| `Ctrl+F`      | Search                            |

---

### 🕹️ COMMAND Mode (Navigation)

| Key           | Action                            |
|---------------|-----------------------------------|
| `W/A/S/D`     | Move cursor up/left/down/right    |
| `Q`           | Jump to start of previous word    |
| `E`           | Jump to start of next word        |

#### Jump Commands (`J + Key`)

| Keys          | Action                            |
|---------------|-----------------------------------|
| `J + Q`       | Top of file                       |
| `J + E`       | Bottom of file                    |
| `J + W`       | Page up                           |
| `J + S`       | Page down                         |
| `J + A`       | Start of line                     |
| `J + D`       | End of line                       |
| `J + K`       | Half page up                      |
| `J + L`       | Half page down                    |
| `J + J`       | Jump to line (enter number)       |

#### Toggle Commands (`T + Key`)

| Keys          | Toggle                            |
|---------------|-----------------------------------|
| `T + N`       | Line numbers                      |
| `T + M`       | Word wrap                         |
| `T + S`       | Syntax highlighting               |
| `T + A`       | Auto-save                         |
| `T + O`       | Mouse support                     |
| `T + B`       | Status bar                        |
| `T + H`       | Help screen                       |
| `T + C`       | Comment selected lines            |
| `T + U`       | Uncomment selected lines          |

---

### 🧩 Selection & Deletion

| Key           | Action                            |
|---------------|-----------------------------------|
| `H`           | Select current line               |
| `L`           | Extend selection to next word     |
| `K`           | Shrink selection from end         |
| `Ctrl+D`      | Delete current line / selection   |
| `Ctrl+K`      | Delete to start of word           |
| `Ctrl+L`      | Delete to end of word             |
| `Ctrl+X`      | Cut selection                     |
| `Ctrl+C`      | Copy selection                    |
| `Ctrl+V`      | Paste clipboard                   |
| `Ctrl+A`      | Select all                        |
| `Tab`         | Insert four spaces                |
| `Backspace`   | Delete before cursor              |
| `Delete`      | Delete at cursor                  |
| `Enter`       | Insert newline with auto-indent   |

---

### ✍️ WRITE Mode

- Printable characters: Insert at cursor
- `Backspace`, `Delete`: As above
- `Enter`: Auto-indented new line (e.g., after `:` in Python)

#### Navigation Keys

| Key           | Action                            |
|---------------|-----------------------------------|
| `Arrow Keys`  | Move in all directions            |
| `Home`        | Start of line                     |
| `End`         | End of line                       |
| `Page Up`     | Scroll up                         |
| `Page Down`   | Scroll down                       |
| `Ctrl+V`      | Paste clipboard                   |
| `Ctrl+D`      | Duplicate line or selection       |
| `Ctrl+W`      | Delete to start of word           |
| `Ctrl+X`      | Cut selection                     |
| `Ctrl+C`      | Copy selection                    |
| `Ctrl+A`      | Select all                        |
| `Tab`         | Insert four spaces                |

---

### 🖱️ Mouse Controls

_Mouse support must be enabled (default: on). Toggle with `T + O`._

| Action             | Description                                |
|--------------------|--------------------------------------------|
| Left Click         | Move cursor / Start selection              |
| Double Left Click  | Select word                                |
| Drag Left Click    | Extend selection                           |
| Scroll Wheel Up    | Scroll up 3 lines                          |
| Scroll Wheel Down  | Scroll down 3 lines                        |

---

### 🔍 Search Mode (`Ctrl+F`)

| Key           | Action                            |
|---------------|-----------------------------------|
| `Ctrl+F`      | Enter search mode                 |
| Characters    | Add to query                      |
| `Enter`       | Confirm search                    |
| `ESC`         | Cancel search                     |
| `↑ / ↓`       | Navigate results                  |
| `Backspace`   | Remove last character             |

---

**More control docs and examples coming soon.**
