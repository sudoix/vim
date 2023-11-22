| key(for cutting and pasting)  | function                                                                       |
| ----------------------------- | ------------------------------------------------------------------------------ |
| yy                            | copy (yank, cut) the current line into the buffer                              |
| Nyy or yNy                    | copy (yank, cut) the next N lines, including the current line, into the buffer |
| p                             | put (paste) the line(s) in the buffer into the text after the current line     |
| P                             | put (paste) the line(s) in the buffer into the text before the current line    |

### searching

| key      | function                                                       |
| -------- | -------------------------------------------------------------- |
| /string  | search forward for occurrence of string in text                |
| ? string | search backward for occurrence of string in text               |
| n        | move to next occurrence of search string                       |
| N        | move to next occurrence of search string in opposite direction |

### replacing

| key             | function                                                    |
| --------------- | ----------------------------------------------------------- |
| :s/old/new/     | replace first old with new in just that  line               |
| :s/old/new/g    | replace all old with new in just that  line                 |
| :%s/old/new/g   | replace all old with new throughout file                    |
| :%s/old/new/gc  | replace all old with new throughout file with confirmations |
| :%s/old/new/gic | same as above but case insensitive                          |
| :noh            | remove highlighting of search matches                       |
