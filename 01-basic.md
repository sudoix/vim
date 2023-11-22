
### vi

The vi editor (visual editor) is almost certainly on every Linux and UNIX system. In fact, if a system has just one editor, it’s probably vi, so it’s worth knowing your way around in vi.

Using vi editor, we can edit an existing file or create a new file from scratch. we can also use this editor to just read a text file.

> vi editor is great even trough ssh sessions!

#### vi or vim ?

 Most Linux distributions now ship with the vim (for **V**i **IM**proved) editor rather than classic vi. Vim is upward compatible with vi and has a graphical mode available (gvim) as well as the standard vi text mode interface. The `vi` command is usually an alias or symbolic link to the vim program.

 There are several versions of vim: tiny, small, normal, big, and huge. We can find out what version of vim we are running and what features are included by using the command(ubuntu 16.04 here ):

```
root@ubuntu16-1:~# vi --version
VIM - Vi IMproved 7.4 (2013 Aug 10, compiled Nov 24 2016 16:44:48)
Included patches: 1-1689
Extra patches: 8.0.0056
Modified by pkg-vim-maintainers@lists.alioth.debian.org
Compiled by pkg-vim-maintainers@lists.alioth.debian.org
Huge version without GUI.  Features included (+) or not (-):
+acl             +farsi           +mouse_netterm   +tag_binary
+arabic          +file_in_path    +mouse_sgr       +tag_old_static
+autocmd         +find_in_path    -mouse_sysmouse  -tag_any_white
-balloon_eval    +float           +mouse_urxvt     -tcl
-browse          +folding         +mouse_xterm     +terminfo
++builtin_terms  -footer          +multi_byte      +termresponse
+byte_offset     +fork()          +multi_lang      +textobjects
+channel         +gettext         -mzscheme        +timers
...
```

Inorder to read, create or modify a file with vi, give the file name to it:

```
vi filename
```

{% hint style="info" %}
**if you just type vi(m) and hit enter, the vi(m) version will be displayed:**

```
                              VIM - Vi IMproved                                
~                                                                               
~                               version 7.4.1689                                
~                           by Bram Moolenaar et al.                            
~           Modified by pkg-vim-maintainers@lists.alioth.debian.org             
~                 Vim is open source and freely distributable                   
~                                                                               
~                        Help poor children in Uganda!                          
~                type  :help iccf<Enter>       for information                  
~                                                                               
~                type  :q<Enter>               to exit                          
~                type  :help<Enter>  or  <F1>  for on-line help                 
~                type  :help version7<Enter>   for version info        
```
{% endhint %}

Okey lets start learning vi(m):

### vi modes

Vim actually has three modes: **insert mode**, **command mode**, and **escape** ** (last-line) mode**. Let’s start with the default mode you’ll see when you start up Vim–command mode.

* **command mode** :  When you run vim filename to edit a file, Vim starts out in command mode. This means that all the alphanumeric keys are bound to commands, rather than inserting those characters.(save, quit, search/replace, navigate around, execute macros,...)
* **insert mode** :  _To enter the insert mode, type i (for “insert”)_ and now the keys will behave as you’d expect. You can type normally until you want to make a correction, save the file, or perform another operation that’s reserved for command mode or escape (last-line) mode. _To get out of insert mode, hit the Escape key._
* **escape (last-line) mode** :  Once you press Escape, you’re in command mode again. What if you’d like to save your file or search through your document? No problem, _press : and Vim will switch to escape (last-line) mode_. Vim is now waiting for you to enter a command like :w to write the file or :q to exit the editor.
If that all sounds complicated, it’s really not. It does take a few days to start training your brain to move between the modes and memorizing the most important keys for movement, commands, and so on.

####  Moving the cursor 

The first thing you’ll want to learn is how to move around a file. When you’re in command mode, you’ll want to remember the following keys and what they do:

| Key    | function                                                       |
| ------ | -------------------------------------------------------------- |
| h      | Move left one character on the current line                    |
| j      | Move down to the next line                                     |
| k      | Move up to the previous line                                   |
| l      | Move right one character on the current line                   |
| w      | Move to the next word on the current line                      |
| e      | Move to the next end of word on the current line               |
| b      | Move to the previous beginning of the word on the current line |
| Crtl-f | Scroll forward one page                                        |
| Ctrl-b |  Scroll backward one page                                      |

>  If you type a number before any of these commands, then the command will be executed that many times. This number is called a _repetition count_ or simply _count_. For example, 5h will move left five characters. You can use repetition counts with many vi commands.

#### Jumping  <a href="moving-to-lines" id="moving-to-lines"></a>

| key | function                 |
| --- | ------------------------ |
| H   | move to top of screen    |
| M   | move to middle of screen |
| L   | move to bottom of screen |

| key | function                                                              |
| --- | --------------------------------------------------------------------- |
| W   | jump forwards to the start of a word (words can contain punctuation)  |
| E   | jump forwards to the end of a word (words can contain punctuation)    |
| B   | jump backwards to the start of a word (words can contain punctuation) |

| key | function                                          |
| --- | ------------------------------------------------- |
| 0   | jump backwards to the start of line               |
| ^   | jump to the first non-blank character of the line |
| $   | jump to the end of the line                       |
| g\_ | jump to the last non-blank character of the line  |
| gg  | go to the first line of the document              |
| G   | go to the last line of the document               |
