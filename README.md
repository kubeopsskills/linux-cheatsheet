# KubeOps Linux CheatSheet
<img src="./assets/logo.png" width="26%" height="26%"/>

This is Day to Day Work Linux Cheatsheet for Software Engineers.

**Facebook:** [Link](https://facebook.com/kubeopsskills)

**Youtube:** [Link](https://www.youtube.com/c/kubeopsskills)

## Directory Commands
| Name   |   Command |
|------------ | -------------|
|Create Directory|mkdir <directory_name>
|Create Directory with Parent|mkdir -p <parent_directory_name>/<directory_name>|
|Remove Directory|rm -r <directory_name>
|Remove Directory without prompt|rm -rf <directory_name>
|Copy Directory|cp -r <directory_name> <destination_path>
|Move Directory|mv <directory_name> <destination_path>

## Search Commands
| Name   |   Command |
|------------ | -------------|
|Search files in a directory|find <directory_name> -name <file_name_pattern>|
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
|List files in current directory|ls
|List files, hidden files in current directory|ls -a
|List files in current directory with their permissions and sizes|ls -l
|List files in current directory with their permissions, sizes, units|ls -lh
|Paginate the content of file|cat <file_name> `\|` less

## File Permissions Commands
| Name   |   Command |
|------------ | -------------|
|Change file permission with permission number|chmod 755 <file_name>
|Change directory permission with permission number|chmod -R 755 <directory_name>
|Change directory permission with letters|chmod -R u+rw,g+r,o+x <directory_name>

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
|View processes not associated with the terminal| ps -a
|View processes not associated with the terminal and owned by you|ps -aux

## Vi Shortcuts Commands
| Name   |   Command |
|------------ | -------------|
|Edit file|vi <file_name>
|Insert mode   |  i |
|Insert next line| o |
|Insert and move cursor to the end of line| shift + c
|Copy line| yy
|Patse line| p
|Delete line| dd
|Go to the end of file|shift + g
|Search keyword|/ `<keyword>`


## References

**An A-Z Index of Linux command line:** [Link](https://ss64.com/bash/)
