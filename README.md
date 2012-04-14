envee
=====

envee is a light bash script inspired by
[archey](https://bbs.archlinux.org/viewtopic.php?id=87610) and
[screenFetch](https://bbs.archlinux.org/viewtopic.php?id=94169). It currently
can display 4 different Arch Linux ASCII logos, along with information about
the system.

Usage
-----

<pre>
usage: envee [option]

 general options:
   -h, --help                  print this help message and exit
   -v, --version               print version info and exit

 art options:
   -A, --Art=ARTOPT            change the ASCII art
   --gallery                   display all possible ASCII art choices

 color options:
   -a, --art-color=COLOR       change the art color
   -l, --label-color=COLOR     change the label color
   -d, --data-color=COLOR      change the data color

 color choices:
   red, green, yellow, blue, magenta, cyan, white
   r,g,y,b,m,c,w

 variable options:
   -s, --set VAR=VALUE         define new or existing variable

 variable choices:
   host, shell, editor, kernel, cpu, explicit, foreign, term, other

 examples:
   envee -a white -l blue -d white -s WM=dwm
   envee --art-color=magenta --set shell=zsh
   envee --set host=modula-1 --set editor=vim
   envee --Art=poison --art-color=green --label-color=white --data-color=red
</pre>

The Gallery
-----------

To preview all of the different logos, use `envee --gallery`

Set
---

to declare a new label and correspoding value, use the `--set` option:
<pre>
envee --set WM=dwm
</pre>
The `--set` option must be used once for each label. Existing label's values
can be changed: 
<pre>
envee --set shell=/bin/fish
</pre>
When referencing existing labels, they can be set using either uppercase or
lowercase:
<pre>
--set EDITOR=vim
</pre>
is equivalent to
<pre>
--set editor=vim
</pre>


Options
-------

envee can be called with a combination of both short and long options, and
each color can be named by using its first letter The following examples are
all equivalent.
<pre>
--data-color=magenta
--data-color=m
-d magenta
-d m
</pre>


Sample Output
-------------

![Screenshot](http://i.imgur.com/ksVA3.png)
