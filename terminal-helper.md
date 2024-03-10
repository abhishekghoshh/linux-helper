# terminal helper


## bash shortcuts


```
# kill active process
ctrl + c


# clear your screen
ctrl + l / cmd + k

# minimize/suspend the current process and come back to the terminal, put process in background
ctrl + z
# reopen the background process
fg


# set the cursor to the first letter/start in the command line, go to front of the line
ctrl + a

# set the cursor to the last letter/end in the command line, go to end of the line
ctrl + e

# go forward one character
ctrl + f

# go backword one character
ctrl + b 

# jump forward by one word
alt + f

# jump backward by one word
alt + b 


# to delete the line starting from the cursor position
ctrl + k 

# to delete a word starting from the current cursor position
alt + d

# delete the line in the command prompt
ctrl + u

# to remove the word backwards from cursor position
ctrl + w


# to paste text from the kill buffer
ctrl + y


# to reverse search for commands you typed in the past from your history, search previous command like fuzzy finder
ctrl + r


# to forward search (works in ZSH for me but not bash)
ctrl + s

# execute previous command
!!

# execute previous command in sudo mode
sudo !!

# run previous matching command
!<command-name>

# open line in the editor
ctrl + x then ctrl + e


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
