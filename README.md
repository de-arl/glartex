# glartex
script to edit latex with gedit and evince, synctex support, native wayland support

The script is made to edit existing tex files that have been compiled as pdf at least once. You need a .tex file and a corresponding pdf in you working directory. It depends on entr (http://eradman.com/entrproject/), tex, gedit and evince. Surely you can use any editor-viewer combination but the chosen one supports wayland and both-way synctex search.

Make the script executable with chmod +x and put it somewhere in your PATH or copy the script to your working directory and execute it with ./glartex

Usage:

run the script with the name of the tex file appended, but without suffix, for example to edit TEXFILE.tex

$ cd path/to/working/directory

$ glartex TEXFILE


If you use sway you can use glartex_sway, it uses glartex_sway_plugin to reorder containers at startup. 





