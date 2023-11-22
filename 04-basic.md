### Exiting

If you’re in insert mode, hit Escape. Then enter : and you’ll see a line at the bottom of the screen with a cursor ready to take input.

| key        | function                                                                     |
| ---------- | ---------------------------------------------------------------------------- |
| :w         |  That will write the file to the existing filename,but don't exit.           |
| :w  _file_ | If you don’t have a filename or want to write out to a different _file name_ |
| :q         | quit (fails if there are unsaved changes)                                    |
| :q!        | Quit editing without saving.                                                 |
| :wq        | write (save) and quit (throw and error if file is not writable)              |
| :wq!       | try to write and quit (if it is not writable, quit without saving! )         |
| ZZ and :x  | Exit and save the file if modified                                           |
| q! or ZQ   | quit and throw away unsaved changes                                          |

Press ESC to return back to the normal command mode!

> When you want to write and exit from a file consider  you permissions, the bellow command write out the current file using sudo:
>
> :w !sudo tee % 
>
> * :w – Write a file (actually buffer). 
> * !sudo – Call shell with sudo command. 
> * tee – The output of write (vim :w) command redirected using tee. 
> * % – The % is nothing but current file name.

### tab and window

| key | function |
| --- | --- |
| :tabnew | new tab |
| :tabnext | next tab |
| :tabprevious |  |
| :new /tmp/file | open new file  |
| ctrl w | change beetween window |
| vimddiff file1 file2 | diff |
| ctrl ww | chage between tow windows |
| :diffget or :diffput | for compair |

### reloading

| key | function                                           |
| --- | -------------------------------------------------- |
| :e  |  (short for `:edit`) reload the file from the disk |
| :e! | it will discard local changes and reload.          |

{% hint style="success" %}
### VIM Tip : running external commands in a shell

It usuaslly happens that we need to run a command in shell to see the result of file which we are edditing. It could be happened in two ways:

1.We could suspend your session (ctrl-Z), and then run the command in your shell.That’s a lot of keystrokes, though !

2.So, instead, you could use vim’s built-in “run a shell command”:

> :!cmd Run a shell command, shows you the output and prompts you before returning to your current buffer.
{% endhint %}

### help

Need help? you can use `:help` or` :help keyword`  and vim will open help for keyword.

