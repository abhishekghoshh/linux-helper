# Neovim helper

```
# practice vim motions 

docker run -it --rm -v $(pwd):/mnt busybox vi /mnt/vim-motion-practice.txt
```


- **Vim motions**
  - **blogs**
  	- [shortcutfoo](https://www.shortcutfoo.com/app/dojos/neovim/cheatsheet)
  	- [devhints](https://devhints.io/vim)
  	- [Vim Cheat Sheet](https://vim.rtorr.com/)
  	- [warp.dev](https://www.warp.dev/topic/vim)
  - **youtube**
    - [Vim Motions for absolute beginners!!!](https://www.youtube.com/watch?v=lWTzqPfy1gE)
      - [Intermediate Vim Motions and Pro Tips!!!](https://www.youtube.com/watch?v=nBjEzQlJLHE)
    - [Vim Tips I Wish I Knew Earlier](https://www.youtube.com/watch?v=5BU2gBOe9RU)
      - [10 Advanced Vim Features (You Probably Didn't Know)](https://www.youtube.com/watch?v=gccGjwTZA7k)
    - [Vim As Your Editor](https://www.youtube.com/playlist?list=PLm323Lc7iSW_wuxqmKx_xxNtJC_hJbQ7R)
    - [Vim Tutorial for Beginners](https://www.youtube.com/watch?v=RZ4p-saaQkc)
  

- **neovim introduction**
  - [PDE: A different take on editing code](https://www.youtube.com/watch?v=QMVIJhC9Veg)
  - [Effective Neovim: Instant IDE](https://www.youtube.com/watch?v=stqUbv-5u2s)
  	- [kickstart.nvim](https://github.com/nvim-lua/kickstart.nvim)
  	- [The Only Video You Need to Get Started with Neovim](https://www.youtube.com/watch?v=m8C0Cq9Uv9o)
  - [Why Neovim nerds are so obsessed with the terminal](https://www.youtube.com/watch?v=5wy2iLU5fs0)
  - [How to ACTUALLY switch from VS Code to Neovim](https://www.youtube.com/watch?v=aCgDs8Nv-jo)
  - [Why I Switched From NEOVIM To VSCODE](https://www.youtube.com/watch?v=U1Mg8E70S6g)
  - [Is This Vim Distribution Superior to VS Code?](https://www.youtube.com/watch?v=nQ2nvTD_46A)
  
- **all neovim configuration**
    - [Learn Neovim The Practical Way](https://alpha2phi.medium.com/learn-neovim-the-practical-way-8818fcf4830f#545a)

- **Neovim tutorial series** 
	- [Neovim from Scratch](https://www.youtube.com/playlist?list=PLhoH5vyxr6Qq41NFL4GvhFp-WLd5xzIzZ)
	- [Neovim for Newbs. FREE NEOVIM COURSE](https://www.youtube.com/playlist?list=PLsz00TDipIffreIaUNk64KxTIkQaGguqn)
	- [Neovim Configuration](https://www.youtube.com/playlist?list=PLsz00TDipIffxsNXSkskknolKShdbcALR)
	- [Beginner Vim](https://www.youtube.com/playlist?list=PLmTrCsxAaghUhCmSiX5Py-e9O8UOPX502)
	- [Coding With Vim](https://www.youtube.com/playlist?list=PLmTrCsxAaghW9KWrzuc6n2B9ud2uV5sjK)
	- [Bash2Basics](https://www.youtube.com/playlist?list=PLep05UYkc6wTWlugE_9Lj6JlLpvSBbkZ_)
	- [Make a Simple Vim/Neovim Plugin from Scratch: cyclist.vim](https://www.youtube.com/watch?v=apyV4v7x33o&list=PLep05UYkc6wSgBFseCsRBSQQ1Fmf3eRa8)

- **Neovim Customization**
	- [The perfect Neovim setup for Go](https://www.youtube.com/watch?v=i04sSQjd-qo)
	- [The perfect Neovim setup for Rust.](https://www.youtube.com/watch?v=mh_EJhH49Ms)
	- [Setting up Neovim for Java Development](https://www.youtube.com/watch?v=8q_VPqA-KLs)
	- [Effective Neovim setup for web development towards 2024](https://www.youtube.com/watch?v=fFHlfbKVi30)
	- [Automatically Execute *Anything* in Nvim](https://www.youtube.com/watch?v=9gUatBHuXE0)
	- [Execute **anything** in neovim (now customizable)](https://www.youtube.com/watch?v=HlfjpstqXwE)
	- [Neovim - Github Copilot | Setup & Demo | Copilot Creates a Simple Game By Itself | Official Plugin](https://www.youtube.com/watch?v=eMnZBaOs4vM&list=PLhoH5vyxr6Qo_5IoxqcQjHgBe77xD5-BP)
	- [Better than Copilot? This AI plugin for Neovim is Incredible](https://www.youtube.com/watch?v=7k0KZsheLP4)

- **Advance topics**
	- [TakeTuesday E03: Introduction to LuaSnip](https://www.youtube.com/watch?v=Dn800rlPIho)
	- [Why Vim Experts Do THIS Instead of Using Tabs...](https://www.youtube.com/watch?v=ST_DZ6yIiXY)


#### Install neovim with lua-jit
```
sudo apt update && sudo apt upgrade -y
sudo apt install ninja-build gettext libtool libtool-bin autoconf automake cmake g++ pkg-config unzip curl
git clone https://github.com/neovim/neovim.git
cd neovim && git checkout stable
make CMAKE_BUILD_TYPE=Release
sudo make install
echo 'export PATH="$PATH:/path/to/neovim"' >> ~/.zshrc
source ~/.zshrc
```

### Neovim chad
- [Turn VIM into a full featured IDE with only one command](https://www.youtube.com/watch?v=Mtgo-nP_r8Y)
- [NeoVim with NVChad | The most beautiful editor for programming.](https://www.youtube.com/watch?v=Irm2WELYSps)
- [Official documentation](https://nvchad.com/docs/quickstart/install)
- [nvchad github](https://github.com/NvChad/NvChad)
- configs present in `~/.config/nvim/lua/custom`

- **Shortcuts**
  - space + c + h for cheetsheet opening and closing
  - Space -> t -> h (setting themes) [option + control + p/n ]
  - Syntax highlighting [TSInstall #laungage_name] [TSInstallInfo]
  - File explorer [cntrl + n] 
  - m for bookmarking
  - a for adding new file
  - c for copy and p for paste
  - file navigation space + f + f
  - space + f + b for find only opened files
  - Window navigation [ ctrl + h / j / k / l ]
  - Window management [vertical split (:vsp)  split (:sp)] 
  - Tab change (tab) (shift + tab) and close tab ( space + x )
  - Toggle line number [ space + n ]
  - Command line 
    - Horizontal ( space + h )
    - vertical ( space + v )
    - to get out of terminal or jump to other windows from terminal
      - ctrl-x then ctrl-ww
  - fuzzy finder
    - <leader>/space + ff
  - Install all packages with mason
    - :MasonInstallAll



# vim motion cheetsheet

## Things to remember
1. toggle the relative line number, when you want to jump directly to next or previous lines
   1. **in nvchad**
      1. :set rnu
      2. :set nornu
2. Mapping esc to any other key ( caps lock)
3. :normal  (normal mode) change multiple line in the same time
   1. (v 10j) -> :normal Ivar [first select 10 consecutive lines and then insert var at the start]
   2. (v 10j) -> :normal A end; [first select 10 consecutive lines and then append end; at the end]
4. change multiple line in the same time ( from the middle of sentence or at the end )
   1. go to the start of the word then (ctrl + v) then (5l + 10j) then (shift + I) to insert then type your text and press ESC to apply the changes for the next 10 lines
   2. go to the start of the word then (ctrl + v) then (5l + 10j) then (shift + A) to Append then type your text and press ESC to apply the changes for the next 10 lines
   3.**To append a text for the next lines** : (ctrl + v) then press (shift + 4) or $ to selct to the end of the line then use 10 j to select next 10 lines and then (shift + A) to Append and type your changes and press ESC to apply your changes for the next 10 lines.
5. Sometime when we are selecting lines and we forgot the first line then we can use (ctrl + o) which will change the direction of the selecting and select the first line
6. % to go to starting or ending of the parenthesis. We can use it to select the entire content inside those parenthesis, or also we can go to the function


(shift + j) => remove empty lines and append the start of the next line to the end of the current line 


(shift + left arrow) go to the starting of the next word
(ctrl + right arrow) go to the starting of the previous word


(shift + down arrow) go the ending line of the current page
(shift + up arrow) go the starting line of the current page


#### Jump between lines
Press ( or (shift + 9) to go to the start of next line
press ) or (shift + 0) to go to the start of previous line


#### Jump between paragraphs
Press { or (shift + [ ) to go to the start of next empty line
Press } or (shift + ] ) to go to the start of previous empty line

Press [ to go to the start of the first line
Press ] to go to the start of the last line



ctrl + b to move a page screen back or "up"
ctrl + f to move a page screen front or "down"
ctrl + u to move a ½ page screen up.
ctrl + d to move a ½ page screen down.






#### Command Description	
```

# Insert at cursor (goes into insert mode)
i

# Write after cursor (goes into insert mode)
a

# Write at the end of line (goes into insert mode)
A

# Terminate insert mode
ESC	

# Undo last change
u

# Undo all changes to the entire line
U

# Open a new line (goes into insert mode)
o

# Delete line
dd

# Delete 3 lines
3dd

# Delete contents of line after the cursor
D

# Delete contents of a line after the cursor and insert new text. Press ESC key to end insertion.
C

# Delete word
dw

# Delete 4 words
4dw

# Change word
cw

# Delete character at the cursor
x

# Replace character
r

# Overwrite characters from cursor onward
R

# Substitute one character under cursor continue to insert
s

# Substitute entire line and begin to insert at the beginning of the line
S

# Change case of individual character
~

```



# Golang shortcuts
