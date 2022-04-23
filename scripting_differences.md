# Scripting differences
Generally, the base of both shells is similar as zsh is based on bash. However, the scripting differences are quite big if we talk about the code conversion from one shell to another. For example, the code in bash:
```
#!/bin/bash
export PATH=/usr/bin:/bin:/usr/sbin:/sbin

function countArguments() {
    echo "${#@}"
}

wordlist="one two three four five"

echo "normal substitution, no quotes:"
countArguments $wordlist
# -> 5

echo "substitution with quotes"
countArguments "$wordlist"
# -> 1
```
As we can see, bash sees white spaces and separates arguments. However, zsh behaves differently:
```
#!/bin/zsh
emulate -LR zsh # reset zsh options
export PATH=/usr/bin:/bin:/usr/sbin:/sbin

function countArguments() {
    echo "${#@}"
}

wordlist="one two three four five"

echo "normal substitution, no quotes:"
countArguments $wordlist
# -> 1

echo "substitution with quotes"
countArguments "$wordlist"
# -> 1
```
Therefore, it returns 1 and does not see the white spaces. It treats everything as one expression. 

The next example is the arrays. In bash iteration starts the same as in every other language such as C++ or java, thus it starts from 0 and goes to length-1. Zsh range starts from 1 and goes up to length (inclusive). 

Lastly, the one big advantage in scripting has bash. It is an older shell scripting environment and also it is pre-installed almost on every device which uses shell scripting. This being said, it has the biggest community of users and thus the biggest support and script availability. We do not need to write many scripts as many of them are publicly available. Also, the bash support is much bigger and there is a higher chance that you will find a bash expert than zsh. Even though both languages are similar there are differences where code modification is not avoidable and hence this may cause a lot of bumps on the way to getting a fully functional code.

https://scriptingosx.com/2019/08/moving-to-zsh-part-8-scripting-zsh/
https://dev.to/jasmin/a-brief-difference-between-zsh-and-bash-5ebp
