# KubeOps Linux CheatSheet
<img src="./assets/logo.png" width="26%" height="26%"/>

This is Day to Day Work Linux Cheatsheet for Software Engineers.

**Facebook:** [Link](https://facebook.com/kubeopsskills)

**Youtube:** [Link](https://www.youtube.com/c/kubeopsskills)

## Directory Commands
| Name   |   Command |
|------------ | -------------|
|Create Directory||mkdir <directory_name>
|Create Directory with Parent|mkdir -p <parent_directory_name>/<directory_name>|

## Search Commands
| Name   |   Command |
|------------ | -------------|
|Search files in a directory|find <directory_name> -name <file_name_pattern>|
|Search file for any lines that don't include the content|grep -v '<content_pattern>' <file_name>

## Pipes
| Name   |   Command |
|------------ | -------------|
|Send stdout of cmd1 to cmd2|cmd1 | cmd2|
|Send stderr of cmd1 to cmd2|cmd1 |& cmd2|

## File Commands
| Name   |   Command |
|------------ | -------------|
|Show content of the file|cat <file_name>
|Create a file with content|cat `<<EOF >` <file_name><br>#!/bin/bash<br>`<content>`<br>`EOF`
|Create an empty file|touch <file_name>

## File Permissions Commands
| Name   |   Command |
|------------ | -------------|

## File Permissions Numbers
| Name   |   Command |
|------------ | -------------|

## Process Commands
| Name   |   Command |
|------------ | -------------|

## Vi Shortcuts Commands
| Name   |   Command |
|------------ | -------------|

## References

**An A-Z Index of Linux command line:** [Link](https://ss64.com/bash/)