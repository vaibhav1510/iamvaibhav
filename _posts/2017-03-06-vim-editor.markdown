---
layout: post
title:  "Using vim editor"
date:   2017-03-06 21:03:36 +0530
categories: Shell Vim
---
Start with these simple Vim commands to learn shall scripting and regular usgae.

Install VIM Editor on Ubuntu
```
apt-get install vim
```

Open a new or existing file
```
vim <file_name>
```

Insert/Write text into the file
```
i - takes to insert mode.
```

press Esc to return to view mode


Other commands
```
:w - to save file
:q - to quit file
x - to delete a character   
ndd - to cut or del ‘n’ lines (e.g press 10dd to remove 10 lines )
nyy - to copy ‘n’ lines    
p - to paste
u - to undo
```

Delete line starting with "demo"
```
:g/^demo/d
```
