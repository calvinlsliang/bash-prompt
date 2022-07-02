
```
parse_git_branch() {
     git branch 2> /dev/null | sed -e '/^[^*]/d' -e 's/* \(.*\)/ (\1)/'
}

export PS1="\w\[\033[32m\]$(parse_git_branch)\[\033[00m\] $ "
```

<img width="212" alt="image" src="https://user-images.githubusercontent.com/811104/177010342-fe8b23ee-9c51-49dc-8e80-f2f6d4e97953.png">
