# KubeOps Linux CheatSheet
<img src="./assets/logo.png" width="26%" height="26%"/>

This is Day to Day Work Linux Cheatsheet for Software Engineers.

**Facebook:** [Link](https://facebook.com/kubeopsskills)

**Youtube:** [Link](https://www.youtube.com/c/kubeopsskills)

# Copyright

<a rel="license" href="https://creativecommons.org/licenses/by-sa/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://licensebuttons.net/l/by-sa/3.0/88x31.png" /></a><br />This work is licensed under a <a rel="license" href="https://creativecommons.org/licenses/by-sa/4.0/">Creative Commons Attribution-ShareAlike 4.0 International License</a>.

## Info Commands
| Name   |   Command |
|------------ | -------------|
|Display manual page of <command_name>|man <command_name>
|The info about  the <command_name>|info  <command_name>
|List a one-line description of <command_name>|whatis  <command_name>
|Find the location of source|whereis  <command_name>
|Find the location of program in terminal|which  <command_name1>  <command_name2> ...
|Display the info abount the <command_name> bash command|help

## Directory Commands
| Name   |   Command |
|------------ | -------------|
|Create Directory|mkdir <directory_name>
|Create Directory with Parent|mkdir -p <parent_directory_name>/<directory_name>|
|Remove Directory|rm -r <directory_name>
|Remove Directory without prompt|rm -rf <directory_name>
|Remove empty Directory|rmdir <directory_name>
|Copy Directory|cp -r <directory_name> <destination_path>
|Move Directory|mv <directory_name> <destination_path>

## Search Commands
| Name   |   Command |
|------------ | -------------|
|Search files in a directory|find <directory_name> -name <file_name_pattern>|
|Search files in a directory with case-insensitive| find <directory_name> -iname <file_name_pattern>|
|Search files in a directory and execute command on it|find <directory_name> -name <file_name_pattern> -exec `<command>`
|Search text in file|grep `<text>` <file_name>
|Search text in file with line numbers| grep -n `<text>` <file_name>
|Search text in file with case-insensitive| grep -i `<text>` <file_name>
|Search text in file for all patterns given| grep -e `<text>` <file_name>
|Search multiple text with case-insensitive and all pattern given| grep -ie `<text1>` <file_name> -ie `<text2>` <file_name> -ie `<text3>` <file_name> -ie `<textn>` <file_name>
|Search file for any lines that don't include the content|grep -v '<content_pattern>' <file_name>

## Pipes
| Name   |   Command |
|------------ | -------------|
|Send stdout of cmd1 to cmd2|cmd1 `\|` cmd2|
|Send stderr of cmd1 to cmd2|cmd1 `\|&` cmd2|

## File Commands
| Name   |   Command |
|------------ | -------------|
|Show content of the file|cat <file_name>
|Create a file with content|cat `<<EOF >` <file_name><br>#!/bin/bash<br>`<content>`<br>`EOF`
|Create an empty file|touch <file_name>
|Remove file|rm <file_name>
|Remove file without prompt|rm -f <file_name>
|Copy file|cp <file_name> <destination_path>
|Move file|mv <file_name> <destination_path>
|Show first n lines of file|head -n <n> <file_name>
|Show last n lines of file|tail -n <n> <file_name>
|Keep showing last 10 lines of file|tail -f <file_name>
|Show total line in a file|cat <file_name> \| wc -l
|List files in current directory|ls
|List files, hidden files in current directory|ls -a
|List files in current directory with their permissions and sizes|ls -l
|List files in current directory with their permissions, sizes, units|ls -lh
|Paginate the content of file|cat <file_name> `\|` less
|Create symbolic link to source file in current directory|ln -s <file_name>
|Create symbolic link to source file in directory|ln -s <file_name> <directory>
|Extract .tar.gz file|tar -zxvf <file_name>
|See the differences between files|diff <file_a> <file_b>

## File Permissions Commands
| Name   |   Command |
|------------ | -------------|
|Change file permission with permission number|chmod 755 <file_name>
|Change directory permission with permission number|chmod -R 755 <directory_name>
|Change directory permission with letters|chmod -R u+rw,g+r,o+x <directory_name>
|Change file owner |chown <user> <file_name>
|Change file owner with user's login group |chown <user>: <file_name>
|Change directory and its content owner recursively |chown -R <user> <directory_name>

## File Permissions Numbers
| Name   |   Command |
|------------ | -------------|
|4            | read (r)
|2            | write (w)
|1            | execute (x)

## Process Commands
| Name   |   Command |
|------------ | -------------|
|Shows processes for the current shell|ps 
|View all the running processes|ps -A or ps -e
|View all processes associated with the terminal| ps -a
|View all processes associated with the terminal and show user|ps -aux
|Kill specific process id| kill -SIGTERM <process_id> ...
|Lists signal| kill -l
|Kill all processes with specifies name| pkill <process_name>
|Kill all processes with case-insensitive| pkill -i <process_name>
|Kill specific running command| pkill -f <running_command_pattern>
|Kill all processes with specific signal| pkill --signal `<signal>` <process_name>
|Show dynamic real-time processes list of specific user| top -u `<user>`

## Vi Shortcuts Commands
| Name   |   Command |   Animation|
|------------ | -------------| -------------|
|Edit file | vi <file_name> | <img src="./assets/vi/vi-editor.gif" /> |
|Insert mode | i | <img src="./assets/vi/insert.gif" /> |
|Insert next line | o | <img src="./assets/vi/insert-next-line.gif" /> |
|Insert and move cursor to the end of line | shift + a | <img src="./assets/vi/shift+a.gif" /> |
|Copy line | yy | <img src="./assets/vi/copy-and-paste.gif" /> |
|Patse line | p | <img src="./assets/vi/copy-and-paste.gif" /> |
|Change line | cc | <img src="./assets/vi/change-line.gif" /> |
|Delete line | dd | <img src="./assets/vi/delete-line.gif" /> |
|Delete next word | dw | <img src="./assets/vi/delete-next-word.gif" /> |
|Delete previous word | db | <img src="./assets/vi/delete-previous-word.gif" /> |
|Delete at caret | x | <img src="./assets/vi/delete-at-caret.gif" /> |
|Delete current cursor to then end of line | shift + c | <img src="./assets/vi/shift+c.gif" /> |
|Substitute single character | s | <img src="./assets/vi/substitute-character.gif" /> |
|Go to the start of file | gg | <img src="./assets/vi/go-to-top.gif" /> |
|Go to the end of file | shift + g | <img src="./assets/vi/go-to-bottom.gif" /> |
|Go to row |`<row_number>` + gg | <img src="./assets/vi/go-to-row.gif" /> |
|Go to column |`<column_number>` + \ | <img src="./assets/vi/go-to-column.gif" /> |
|Search keyword |/ `<keyword>` | <img src="./assets/vi/search-keyword.gif" /> |
|Search keyword case-insensitive | /\c `<keyword>` | <img src="./assets/vi/search-case-insensitive.gif" /> |
|Search move next | n | <img src="./assets/vi/search-next.gif" /> |
|Search move previous | shift + n | <img src="./assets/vi/search-previous.gif" /> |
|Visualize character| v | <img src="./assets/vi/visualize-character.gif" /> |
|Visualize line | shift + v | <img src="./assets/vi/visualize-line.gif" /> |
|Tab right | shift + . | <img src="./assets/vi/tab-right.gif" /> |
|Tab left | shift + , | <img src="./assets/vi/tab-left.gif" /> |
|Repeat last change| . | <img src="./assets/vi/repeat-last-change.gif" /> |
|Undo| u | <img src="./assets/vi/undo.gif" /> |
|Redo| ctrl + r | <img src="./assets/vi/redo.gif" /> |
|Save| :wq | <img src="./assets/vi/save.gif" /> |
|Quit| :q | <img src="./assets/vi/quit.gif" /> |


## References

**An A-Z Index of Linux command line:** [Link](https://ss64.com/bash/)
