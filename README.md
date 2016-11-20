ncl_lazy_vim README
===================

If you are using vi/vim/gvim for scripting with NCL, you can sometimes hardly remember NCL commands or you are just too lazy to type out "gsFillWTF..." all the time, this might be something for you.

![animation]( ncl_completion.gif )

Configuration instructions
--------------------------
1. Download the two .txt files "NCL_functions.txt" and "NCL_resources.txt" from the ".vim" folder in this repository into your ".vim" folder
2. Add the lines of "add_ncl_complete_to_your_vimrc" to your "~/.vimrc" to include the complete function <br>
```
cat add_ncl_complete_to_your_vimrc >> ~/.vimrc
```
If you don't have a .vimrc file yet, you may also just my working example "example.vimrc" and rename it in your $HOME <br>

Optional: <br>
1. Variable completion: Set a file path and 'ENABLE' vars_completion in your ".vimrc" <br> - requires CDO - if you have a neat idea how to implement it with NCL commands please approach me
![animation]( vars_completion.gif ) <br>
2. For now, the first 12 (random number) words of NCL Resources are displayed in the pop-up window before the last two words as "Default information" separated by "...". If you usually work on a wide vi window, you can modify this number of strings. <br>
3. If you fancy other auto-completion setting, play with the line
```
set complete=longest,menuone
```
The current setting completes up to the last common string and then shows a menu. Other options are listed in the vim help or http://vimdoc.sourceforge.net/htmldoc/options.html#'completeopt' <br>

<br>

Syntax highlighting:
* coming soon dynamical hopefully <br> for now data from Version 6.3.0 - https://www.ncl.ucar.edu 

Snippets: 
* copy "ncl.snippets" into "/.vim/bundle/vim-snippets/snippets" after you installed the vim plugin snipmate https://github.com/garbas/vim-snipmate

Operating instructions
----------------------
Start typing your desired cdo command and hit &lt;Control-X>&lt;Control-U>
```
res@gsF<Ctrl-X><Ctrl-U>
addf<Ctrl-X><Ctrl-U>
```
Get the following autocompletion options 
```
gsFillBackgroundColor   NCL Res: This resource of type ... Default: Transparent
gsFillColor             NCL Res: This resource of type ... Default: Foreground
or
addfile                 NCL Func.: 
addfiles                NCL Func.:
or
<ncl_command>           <type>: <description>         ... Default: <value>
...
```
Hit &lt;Ctrl-N> go get the first shown match
```
res@gsFillBackgroundColor
or
addfile
```
Hit another &lt;Ctrl-N> to choose the next match or move down with arrow keys and hit <Enter> for your choice 



Copyright and licensing information
-----------------------------------
* MIT

Known bugs
----------
* static ncl data

Contact information
-------------------
Aaron Spring <br> Bundesstraße 53 <br> ZMAW Room 229 <br> aaron.spring@mpimet.mpg.de <br> <br> 
Looking forward to receiving your questions, comments or wishes


Changelog
---------
* v0.1: 
uses all NCL resources and NCL functions from website as of 2016/09/18 <br>
also completes variables gathered by 'cdo vardes files' if cdo installed and vars_completion enabled <br>
requires '*.ncl' files <br>
ncl_completion can be enabled or disabled in .vimrc <br> 
* v0.2:
static snippets and static syntax highlighting

Working on
----------
* syntax highlighting
* getting functions and resources dynamically, see example uses 'cdo --operators' https://github.com/aaronspring/cdo_lazy_vim
* snippets
* anything else needed?

Credits and acknowledgements
----------------------------
* Prince K Xavier, the dude who set up auto-completion for NCL and made me think to do this for CDO first and now I'm back to NCL
 

Sister project
--------------
* same stuff for CDO: https://github.com/aaronspring/cdo_lazy_vim
