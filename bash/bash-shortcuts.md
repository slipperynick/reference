# Bash Keyboard Shortcuts

## Moving the Cursor
- **Ctrl + A** → Go to the beginning of the line (Home)  
- **Ctrl + E** → Go to the end of the line (End)  
- **Ctrl + P** → Previous command (Up arrow)  
- **Ctrl + N** → Next command (Down arrow)  
- **Alt + B** → Move back (left) one word  
- **Alt + F** → Move forward (right) one word  
- **Ctrl + F** → Move forward one character  
- **Ctrl + B** → Move backward one character  
- **Ctrl + XX** → Toggle between the start of the line and current cursor position  

## Editing
- **Ctrl + L** → Clear the screen (similar to `clear` command)  
- **Alt + Del** → Delete the word before the cursor  
- **Alt + D** → Delete the word after the cursor  
- **Ctrl + D** → Delete the character under the cursor  
- **Ctrl + H** → Delete the character before the cursor (Backspace)  
- **Ctrl + W** → Cut the word before the cursor to the clipboard  
- **Ctrl + K** → Cut the line after the cursor to the clipboard  
- **Ctrl + U** → Cut/delete the line before the cursor to the clipboard  
- **Alt + T** → Swap current word with the previous word  
- **Ctrl + T** → Swap the last two characters before the cursor (typo fix)  
- **Esc + T** → Swap the last two words before the cursor  
- **Ctrl + Y** → Paste the last thing that was cut (yank)  
- **Alt + U** → UPPERCASE all characters from the cursor to the end of the word  
- **Alt + L** → Lowercase all characters from the cursor to the end of the word  
- **Alt + C** → Capitalize the character under the cursor and move to the end of the word  
- **Alt + R** → Cancel changes and restore the previous line from history  
- **Ctrl + _** → Undo  

## Tab Completion
- **TAB** → Auto-completes file/directory names  
  - Example: To move to a directory named `sample1`, type `cd sam` then press **TAB** and **ENTER**  

## Command History
- **Ctrl + R** → Recall last command containing specified characters (searches history as you type)  
- **Ctrl + P** → Previous command in history (walk back through history)  
- **Ctrl + N** → Next command in history (walk forward through history)  
- **Ctrl + S** → Search forward in history (beware: may pause terminal output, use `Ctrl + Q` to resume)  
- **Ctrl + O** → Execute the command found via `Ctrl + R` or `Ctrl + S`  
- **Ctrl + G** → Escape from history search mode  
- **!!** → Repeat last command  
- **!abc** → Run last command starting with `abc`  
- **!abc:p** → Print last command starting with `abc`  
- **!$** → Use the last argument from the previous command  
- **ALT + .** → Use the last argument from the previous command  
- **!* ** → Use all arguments from the previous command  
- **^abc^def** → Run previous command, replacing `abc` with `def`  

## Process Control
- **Ctrl + C** → Interrupt/Kill the running process (SIGINT)  
- **Ctrl + L** → Clear the screen  
- **Ctrl + S** → Stop output to the screen (useful for long-running verbose commands)  
- **Ctrl + Q** → Resume output to the screen (if previously stopped with `Ctrl + S`)  
- **Ctrl + D** → Send an EOF marker (this closes the current shell unless disabled)  
- **Ctrl + Z** → Suspend the current task (SIGTSTP), resume later with `fg`  

## Emacs Mode vs Vi Mode
By default, Bash runs in **Emacs mode**, but you can switch to **Vi mode**:  
- **Set Vi Mode in Bash:**  
  `$ set -o vi`
- **Set Emacs Mode in Bash:**  
  `$ set -o emacs`

---
