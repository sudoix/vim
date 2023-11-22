### Editing text <a href="editing-text" id="editing-text"></a>

Now that you can open a file in vi, move around it and get out, it’s time to learn how to edit the text in the file

| key( for inserting) | function                                                       |
| ------------------- | -------------------------------------------------------------- |
| i                   | insert text before cursor, until  hit                          |
| I                   | insert text at beginning of current line, until  hit           |
| a                   | append text after cursor, until  hit                           |
| A                   | append text to end of current line, until  hit                 |
| o                   | open and put text in a new line below current line, until  hit |
| O                   | open and put text in a new line above current line, until  hit |

| key(for changing) | function                                                                                    |
| ----------------- | ------------------------------------------------------------------------------------------- |
| r                 | replace single character under cursor (no  needed)                                          |
| R                 | replace characters, starting with current cursor position, until  hit                       |
| cw                | change the current word with new text, starting with the character under cursor, until  hit |
| cNw               | change N words beginning with character under cursor, until  hit; e.g., c5w changes 5 words |
| C                 | change (replace) the characters in the current line, until  hit                             |
| cc                | change (replace) the entire current line, stopping when  is hit                             |
| Ncc or cNc        | change (replace) the next N lines, starting with the current line, stopping when  is hit    |

| key (for deleting) | function                                                                        |
| ------------------ | ------------------------------------------------------------------------------- |
| x                  | delete single character under cursor                                            |
| Nx                 | delete N characters, starting with character under cursor                       |
| dw                 | delete the single word beginning with character under cursor                    |
| dNw                | delete N words beginning with character under cursor; e.g., d5w deletes 5 words |
| d^                 | delete  start of line till the cursor                                           |
| d$ and D           | delete the remainder of the line, starting with current cursor position         |
| dd                 | delete entire current line                                                      |
| Ndd or dNd         | delete N lines, beginning with the current line; e.g., 5dd deletes 5 lines      |