---
layout: default
title: "Tokens"
parent: "Sarvar"
nav_order: 4
---
### Tokens
Each token is consisted of:
```
globalvars (dict[str, str]): Global variables accessible throughout execution
privatevars (list[str]): Private variables for current scope
args (list[str]): List of command arguments
macros (dict[str, str]): Defined macro replacements
current_line (int): Current line being executed
all_lines (int): Total number of lines in program
````
`privatevars` is the command line arguments for the specified or detected command\
\
`args` push or append or insert a command to be handeled in the debug list\
\
`macros` list of all macros\
\
`current_line` Current line this command being executed on\
\
`all_lines` All of the lines that is in the current command's execution scope\
\
`globalvars` All of the variables defined by other commands