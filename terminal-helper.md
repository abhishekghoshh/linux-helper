# terminal helper


## bash shortcuts


```
# kill active process, stops the current in-progress command
# Kill whatever you are running. Also clears everything on current line
ctrl + c

# Exit the current shell when no process is running, or send EOF to a the running process
ctrl + d

# minimize/suspend the current process and come back to the terminal, put process in background
ctrl + z
# reopen the background process
fg


# Up arrow shows previous commands


# clear your screen
ctrl + l / cmd + k




# Tab automatically completes commands




# set the cursor to the first letter/start in the command line, go to front of the line
ctrl + a

# set the cursor to the last letter/end in the command line, go to end of the line
ctrl + e

# go forward one character
ctrl + f

# go backword one character
ctrl + b 

# Move cursor one word forward, jump forward by one word
alt + f   /   Option + →

# Move cursor one word backward, jump backward by one word
alt + b   /   Option + ←



# Swap the last two characters before the cursor (not working in mac, it is showing a list of files as fuzzy finder)
ctrl + t

# Swap the last two words before the cursor
esc + t



# Cut everything backwards to beginning of line, delete the line in the command prompt
ctrl + u

# to remove the word backwards from cursor position
ctrl + w

# Cut one word backwards using none alphabetic characters as delimiters
esc + backspace

# Cut everything forward to end of line, to delete the line starting from the cursor position
ctrl + k 

# to delete a word starting from the current cursor position
alt + d

# delete one character
ctrl + h

# Paste whatever was cut by the last cut command, to paste text from the kill buffer
ctrl + y

# Undo the last command. (Underscore. So it's actually Ctrl + Shift + minus)
ctrl + _  (Ctrl + Shift + minus)







#### zsh terminal specific

# create a new tab zsh terminal 
cmd + t

# switch tab in zsh terminal
ctrl + tab    /      ctrl + shift + tab
cmd + left arraow  /   cmd + right arrow
cmd + shift + [     /    cmd + shift + ]

# split the window horizonatally in zsh terminal
cmd + d

# split the window vertically in zsh terminal
cmd + shift + d

switch between splitted tabs 
cmd + [    /     cmd + ]

# close the current tab in zsh terminal
cmd + w
```


```
# you can create alias and add it to the bashrc or zshrc

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


# single line push
function push() {
  git add . && git commit -m "$*" && git push
}
```


- **mac**
  - [50 macOS Tips and Tricks Using Terminal (the last one is CRAZY!)](https://www.youtube.com/watch?v=qOrlYzqXPa8)
- **linux**
  - [7 Essential Command Line Tools (2022)](https://www.youtube.com/watch?v=2OHrTQVlRMg)
  - [5 Linux Terminal Applications You Need](https://www.youtube.com/watch?v=E8Ww39z_28A)
- **mac & linux**
  - [6 AWESOME Command Line Tools For MAC And LINUX](https://www.youtube.com/watch?v=szehPBOwqlI)
- **windows**
  - [Make Windows Terminal look amazing!](https://www.youtube.com/watch?v=AK2JE2YsKto)
  - [Make Windows Terminal Look Better | Oh My Posh Guide](https://www.youtube.com/watch?v=-G6GbXGo4wo)


```


```
