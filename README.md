=== GLARTEX VERSION 0.4 ===

Glartex is a commandline utility to edit latex-Documents with your favorite editor and your favorite pdf-viewer.
 
This enables latex editing with the programms you are most productive with, or editing latex in pure wayland sessions.

Glartex will open all the programms you need for your latex-session and it will watch the tex-file you edit: Everytime the file is changed, it will be compiled.

Glartex supports latex, bibtex, synctex and it has built-in functions to invoke a translation shell or move windows to your preffered workspaces if you use sway.


INSTALLATION:

Install entr (eradman.com/entrproject/)

If you want to use the translate option install the translate shell (soimort.org/translate/shell/)

Copy glartex_v0.4 to ~/.config/glartex

Add ./config/glartex/scripts to your PATH or copy the executables into your PATH

To get forward and backward search with vim or gvim and zathura run the install script in glartex/install_zathura_vim_synctex

Edit the config file to your liking


USAGE:

glartex [-e editor] [-v viewer] [-b 0/1] [-s 0/1] [-o 0/1] [-x] [-t TL] <-f/-c/-C FILE>

	-e editor	Set editor
	-v viewer	Set viewer
	-b 0/1	Set bibtex false/true
	-s 0/1	Set synctex false/true
	-o 0/1	Set swaymode false/true
	-x	Same as -b 1 -s 1 -o 1
	-t TL	Include translate shell with target language TL
	-n NAME	Rename output
	-N NAME	Rename output and redirect to ./NAME_yy-mm-dd

	---Options override defaults from configfile---

	-f FILE	Edit any file
	-c FILE	Edit copy of file in working directory
	-C FILE	Edit copy of file in new directory ./FILE_yy-mm-dd

	-h 	Help


glartex -T TEMPLATE

	Edit template in working directory

	To edit template in new directory use $glartex -C path/to/template


glartex FILENAME

	If file exists:
	Same as -f FILENAME

	If file doesn't exist:
	Edit a copy of DEFAULT_TEMPLATE named FILENAME in new directory ./FILENAME_yy-mm-dd


IMPORTANT:

	Glartex sources ~/.config/glartex/config
	Templates are in ~/.config/glartex/templates
	Depends on entr github.com/clibs/entr
	Translate option depends on translate shell github.com/soimort/translate-shell
    Synctex for sure works with gedit and evince as well as with vim and zathura, if you need another combination, please email me

	To change -o behaviour edit function swayorder

AUTHOR:

	de-arl, suspu@protonmail.com

München 27.02.2020
