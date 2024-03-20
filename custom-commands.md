# custom command made using alias



#### you can create alias and add it to the bashrc or zshrc
```
alias i="sudo apt install "
alias weather="curl wttr.in"

alias cheat="curl https://cheat.sh/$1"  # this will not work because alias do not take parameter directly 
# we could add a function in the .bashrc/.zshrc
cheat() {
    curl "https://cheat.sh/$1"
}
# thn we can use like cheat rsync
```


#### Some of my custom created commands
```

alias bat='bat --paging=never'

alias ls='lsd'

# view files in preview with fuzzy finder
alias fcat='fzf --preview "cat {}"'

# view files with bat in preview with fuzzy finder
fbat() {
  local file
  file=$(fzf --preview "bat --style=plain --color=always {}" --preview-window=right:50%:wrap)
  if [[ -n $file ]]; then
    bat --style=plain --color=always "$file"
  fi
}

# cd with fuzzy finder
cd_fzf() {
  local dir
  dir=$(find * -type d 2>/dev/null | fzf --preview 'ls -l {}' --height 40%)
  [ -n "$dir" ] && cd "$dir"
}
alias fd=cd_fzf


# this will fuzzyfind any commands manual page
alias fman=compgen -c | fzf | xargs man


# single line git push
function push() {
  if [ -z "$1" ]; then
    git push
  else
    git add . && git commit -m "$1" && git push
  fi
}

```