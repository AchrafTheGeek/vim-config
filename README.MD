First make these following directories 

$ mkdir -p ~/.vim ~/.vim/autoload ~/.vim/backup ~/.vim/colors ~/.vim/plugged


Create a .vimrc file in your home directory.

$ touch ~/.vimrc



First let's add some basic settings that will improve your editing experience. I use double quote characters to comment out lines.

Add the following lines to your .vimrc file:
" Disable compatibility with vi which can cause unexpected issues.
set nocompatible

" Enable type file detection. Vim will be able to try to detect the type of file in use.
filetype on

" Enable plugins and load plugin for the detected file type.
filetype plugin on

" Load an indent file for the detected file type.
filetype indent on



Syntax highlighting is very useful. The next line we add will enable syntax highlighting and make your code easier to read.

" Turn syntax highlighting on.
syntax on



Remap the capslock key to ESC key when launching VIM and reset it after closing VIM: 

au VimEnter * !xmodmap -e 'clear Lock' -e 'keycode 0x42 = Escape'
au VimLeave * !xmodmap -e 'clear Lock' -e 'keycode 0x42 = Caps_Lock'