# Neovim helper

```
# practice vim motions 

docker run -it --rm -v $(pwd):/mnt busybox vi /mnt/vim-motion-practice.txt
```


- **Vim mostions**
	- [shortcutfoo](https://www.shortcutfoo.com/app/dojos/neovim/cheatsheet)
	- [devhints](https://devhints.io/vim)
	- [Vim Cheat Sheet](https://vim.rtorr.com/)
  

- **vim introduction**
  - [Vim Motions for absolute beginners!!!](https://www.youtube.com/watch?v=lWTzqPfy1gE)
  - [Vim Tutorial for Beginners](https://www.youtube.com/watch?v=RZ4p-saaQkc)
  - [PDE: A different take on editing code](https://www.youtube.com/watch?v=QMVIJhC9Veg)
    - [Effective Neovim: Instant IDE](https://www.youtube.com/watch?v=stqUbv-5u2s)
    	- [kickstart.nvim](https://github.com/nvim-lua/kickstart.nvim)
  - [Vim As Your Editor](https://www.youtube.com/playlist?list=PLm323Lc7iSW_wuxqmKx_xxNtJC_hJbQ7R)
  
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

