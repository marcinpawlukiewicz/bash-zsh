# Key bindings
Key bindings is nothing more than our shortcuts on the keyboard to make our life simplest. For example, **CTRL+A** will throw us at the beginning of the line which is very useful if the line is long and the mistake was made at the beginning of our code. 

Both bash and zsh can be configured and have the same key bindings. The main difference is the syntax, both operate on a different one and command configuration looks a bit different. This is an example of this configuration: 

.inputrc for bash:
```
"\C-p": history-search-backward
"\C-n": history-search-forward
"\e[A": history-search-backward
"\e[B": history-search-forward
```

And the same commands for zsh in zle:
```
# You may want to call different history search commands, e.g.
# down-line-or-history or down-line-or-search (and up-*)
bindkey '^P' history-search-backward
bindkey '^N' history-search-forward
bindkey '\e[A' history-search-backward
bindkey '\e[B' history-search-forward
```
https://unix.stackexchange.com/questions/19426/keyboard-bindings-from-bash-to-zsh

Here are some useful commands that have been already bind:
1. **ALT+A** - Go to the beginning of a line.  
2. **ALT+B** - Move one character before the cursor.  
3. **ALT+C** - Suspends the running command/process.   
4. **ALT+D** - Closes the empty Terminal (I.e it closes the Terminal when there is nothing typed). Also deletes all characters after the cursor.  
5. **ALT+F** - Move forward one character.  
6. **ALT+T** - Swaps the last two words.  
7. **ALT+U** - Capitalize all characters in a word after the cursor.  
8. **ALT+L** - Uncaptalize all characters in a word after the cursor.  
9. **ALT+R** - Undo any changes to a command that you have brought from the history if you’ve edited it.  
10. **ALT+.** (note the dot at the end) - Use the last word of the previous command.  

For Mac users on zsh those commands work with left control.

https://ostechnix.com/list-useful-bash-keyboard-shortcuts/
