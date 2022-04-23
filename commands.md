# Commands
When I was comparing bash and zsh my conclusion was simple, they use the same commands. So now, what is the difference?

1. Zsh autocompletion is faster than bash but this is not a big difference in time, and when we use simple commands I don’t think it is noticeable.
1. Zsh has an autocompletion feature while bash needs a bash-completion package. For zsh default setting is set to off. Once you turn this on by adding the following command to the .zsh file:
```
ENABLE_CORRECTION="true"
```
And then, for example if we type something incorrectly:
```
sl -la /tmp
zsh: correct 'sl' to 'ls' [nyae]?
```
Where n - no, y - yes, a - abort, e - edit.  
It is a very convenient feature, especially when our lines are getting longer[^footnote1].   

Those are two major differences I found. Many sources give an information about wildcard (usage of * as a word) as not accessible for bash. However, I checked this on multiple versions of bash, and for all of the,m I had this feature on by default. 

However, there are a couple of features provided by zsh that bash does not have and can be invoked by commands and proper configuration of the .zsh file in our main directory (~). For example, the zmv command can help with massive either file or directory name changes. It is a game-changer if we have hundreds of files. Another useful feature is the build-in calculator activated by a simple command zcalc. Now, you can do simple calculations without leaving your terminal {cite}`ruby`.

**Sources:**   
```{bibliography}```
{bibliography}
\bibliography{stackabuse}
https://stackabuse.com/zsh-vs-bash/   
https://hands-on.cloud/which-terminal-is-better-bash-vs-zsh/

[^footnote1]: https://blog.confirm.ch/zsh-tips-auto-completion-correction/
