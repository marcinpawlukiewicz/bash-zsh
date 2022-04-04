# Completion
Most shells so does bash and zsh use tab key to finish either a word or a phrase. This helps us to write faster and avoid a mistake that can ruin the entire command line. 

As it turns out not every bash has this feature enabled (if you don’t you can proceed with the following steps: https://faun.pub/configure-bash-auto-completion-tab-completion-on-linux-db0d9310818b). But once it is on, it is very simple, for example, we want to finish the name of the file we just start writing in the command line, we press tab key and it is done. Zsh works similar and you would say it is exactly the same. And you are right.

However, zsh has much bigger potential and to use it, we need to know how to make the other options available as those options are off as default.  

To start the process we need to be in our main directory (~) and write out:
compinstall

The installation process is very complicated and hard in understanding. If you would like to go through it I encourage you to read this article - https://www.csse.uwa.edu.au/programming/linux/zsh-doc/zsh_23.html.

Now, what different does this feature make? Here are main features provided by completion in zsh:
1. Case Insensitive Completion - our shell doesn’t care then about the format of the letter, it treats big and small as one. This can be very useful, especially on macOS as the system files are case insensitive.
1. Partial Completion - you don’t need to type directories in full, here are two examples that give you better understanding:
```
% cd /u/lo/b⇥
% cd /usr/local/bin
```
```
% cd ~/L/P/B⇥
% ~/Library/Preferences/ByHost/
```
3. Commands with Build-in Completion - if we now that we need to use one of the option for the command of our choice and we simply do not remember it, we can find out what are the options by adding “-“ (dash) after the command:
```
% cp -⇥
  -H  -- follow symlinks on the command line in recursive mode
  -L  -- follow all symlinks in recursive mode 
 -P  -- do not follow symlinks in recursive mode (default)
  -R  -- copy directories recursively 
 -X  -- don't copy extended attributes or resource forks
  -a  -- archive mode, same as -RpP 
 -f  -- force overwriting existing file
  -i  -- confirm before overwriting existing file 
 -n  -- don't overwrite existing file
  -p  -- preserve timestamps, mode, owner, flags, ACLs, and extended attributes
 -v  -- show file names as they are copied 
 ```

Lastly, once you know how to work with zsh you may build your own completions and customize your environment as much as you like.

https://scriptingosx.com/2019/07/moving-to-zsh-part-5-completions/
