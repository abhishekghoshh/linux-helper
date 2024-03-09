# Terminal shortcuts




```
# clear your screen
ctrl + l / cmd + k


ctrl + c

# minimize/suspend the current process and come back to the terminal
ctrl + z
# reopen the background process
fg

# delete the line in the command prompt
ctrl + u

# set the cursor to the first letter/start in the command line
ctrl + a

# set the cursor to the last letter/end in the command line
ctrl + e


# execute previous command
sudo !!

# search previous command like fuzzy finder
ctrl + r
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

