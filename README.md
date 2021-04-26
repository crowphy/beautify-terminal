# beautify-terminal
终端美化+快捷命令脚本
```shell
alias gn="git clone"

alias gst="git status"
alias gct="git checkout"
alias gcb="git checkout -b"
alias gcm="git commit -m"
#拉取当前分支
alias gl="git pull"
#拉取当前分支并从master分支rebase
alias glm="git pull --rebase origin master"
#推送到当前分支
alias gp='echo 当前分支： $(git branch --show-current) && git push --force --set-upstream origin $(git branch --show-current)'
#先从master分支rebase再推送到当前分支
gpr () { cd $(git rev-parse --show-toplevel) && git add . && git commit -m "$1" && git pull --rebase origin master && gp }

#解决冲突
alias grc="git add . && git rebase --continue"
alias grs="git add . && git rebase --skip"
alias gra="git add . && git rebase --abort"
```