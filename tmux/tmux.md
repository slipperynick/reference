# Most Used Tmux Commands


## 1. Starting and Attaching Sessions
- `tmux` – Start a new tmux session  
- `tmux new -s <session>` – Create a new named session  
- `tmux a` – Attach to a detached session  
- `tmux a -t <session>` – Attach to a specific session  
- `tmux ls` – List all tmux sessions  
- `tmux kill-session -t <session>` – Kill a specific session  
- `tmux kill-server` – Kill all sessions and exit tmux  
- `tmux rename-session -t <old_name> <new_name>` – Rename a session  

## 2. Detaching and Exiting
- `Ctrl + b, d` – Detach from the current session  
- `Ctrl + b, x` – Close the current pane  
- `Ctrl + b, &` – Close the current window  
- `Ctrl + d` – Exit tmux when only one pane is left  
- `tmux detach-client -s <session>` – Force detach another client from a session  

## 3. Splitting Panes
- `Ctrl + b, "` – Split pane horizontally  
- `Ctrl + b, %` – Split pane vertically  
- `tmux split-window -h` – Split window horizontally from command line  
- `tmux split-window -v` – Split window vertically from command line  

## 4. Navigating Between Panes
- `Ctrl + b, Arrow Key` – Move between panes  
- `Ctrl + b, o` – Switch to the next pane  
- `Ctrl + b, ;` – Toggle between the last two panes  
- `Ctrl + b, Space` – Toggle pane layout  
- `Ctrl + b, {` – Move the current pane left  
- `Ctrl + b, }` – Move the current pane right  

## 5. Resizing Panes
- `Ctrl + b, Hold Arrow` – Resize pane in direction (Up/Down/Left/Right)  
- `Ctrl + b, Alt + Arrow` – Resize pane in small steps  
- `Ctrl + b, Ctrl + Arrow` – Resize pane faster  
- `Ctrl + b, M` – Maximize the current pane  
- `Ctrl + b, z` – Toggle pane zoom  

## 6. Managing Windows
- `Ctrl + b, c` – Create a new window  
- `Ctrl + b, ,` – Rename current window  
- `Ctrl + b, p` – Switch to the previous window  
- `Ctrl + b, n` – Switch to the next window  
- `Ctrl + b, <number>` – Switch to a specific window  
- `Ctrl + b, w` – Display a list of windows  
- `Ctrl + b, f` – Find a window by name  
- `tmux move-window -t <session>:<window_number>` – Move window to another session  

## 7. Copy & Scroll Mode
- `Ctrl + b, [` – Enter copy mode (scroll & select text)  
- `Arrow Keys / PageUp` – Scroll in copy mode  
- `Space` – Start selection  
- `Enter` – Copy selected text  
- `Ctrl + b, ]` – Paste copied text  
- `Ctrl + b, PgUp` – Scroll up  
- `Ctrl + b, PgDn` – Scroll down  

## 8. Searching and Command Mode
- `Ctrl + b, /` – Search for text in the buffer  
- `Ctrl + b, ?` – Search backward in buffer  
- `Ctrl + b, n` – Jump to the next search result  
- `Ctrl + b, N` – Jump to the previous search result  
- `Ctrl + b, :` – Open command prompt (enter tmux commands)  

## 9. Reload Configuration
- `Ctrl + b, : source-file ~/.tmux.conf` – Reload tmux configuration  

## 10. Session Management
- `tmux detach` – Detach from a session  
- `tmux switch -t <session>` – Switch to another session  
- `tmux attach-session -d -t <session>` – Attach and detach others from the session  
- `tmux set -g mouse on` – Enable mouse support  
- `tmux show-messages` – Show messages from the command log  
- `tmux display-panes` – Show pane numbers for quick selection  

---
