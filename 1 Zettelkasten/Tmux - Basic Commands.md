
**Default prefix key:** `Ctrl+b` (shown as `C-b` below)

## Session Management

| Command                     | Description                 |
| --------------------------- | --------------------------- |
| `tmux`                      | Start new session           |
| `tmux new -s name`          | Start new session with name |
| `tmux ls`                   | List sessions               |
| `tmux a` or `tmux attach`   | Attach to last session      |
| `tmux a -t name`            | Attach to named session     |
| `tmux kill-session -t name` | Kill named session          |
| `C-b d`                     | Detach from session         |
| `C-b $`                     | Rename current session      |
| `C-b s`                     | List and switch sessions    |

## Window Management

| Command   | Description                |
| --------- | -------------------------- |
| `C-b c`   | Create new window          |
| `C-b ,`   | Rename current window      |
| `C-b w`   | List windows               |
| `C-b n`   | Next window                |
| `C-b p`   | Previous window            |
| `C-b 0-9` | Switch to window by number |
| `C-b &`   | Kill current window        |
| `C-b f`   | Find window by name        |

## Pane Management

| Command       | Description             |
| ------------- | ----------------------- |
| `C-b %`       | Split pane vertically   |
| `C-b "`       | Split pane horizontally |
| `C-b arrow`   | Navigate between panes  |
| `C-b o`       | Next pane               |
| `C-b ;`       | Toggle last active pane |
| `C-b x`       | Kill current pane       |
| `C-b z`       | Toggle pane zoom        |
| `C-b {`       | Move pane left          |
| `C-b }`       | Move pane right         |
| `C-b space`   | Toggle pane layouts     |
| `C-b !`       | Convert pane to window  |
| `C-b C-arrow` | Resize pane             |

## Copy Mode (Scrollback)

|Command|Description|
|---|---|
|`C-b [`|Enter copy mode|
|`q`|Exit copy mode|
|`Space`|Start selection|
|`Enter`|Copy selection|
|`C-b ]`|Paste buffer|

## Misc Commands

| Command                         | Description          |
| ------------------------------- | -------------------- |
| `C-b ?`                         | List all keybindings |
| `C-b t`                         | Show time            |
| `C-b :`                         | Enter command mode   |
| `tmux source-file ~/.tmux.conf` | Reload config        |

