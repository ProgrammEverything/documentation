---
layout: default
title: "Flags"
parent: "Sarvar"
nav_order: 8
---
#### Flags
Flags for the `self.interpret` function
* `"_attributename_stop"` -> Raises an error when the attributename gets called `(attributes are functions starting with '_' such as '_error_attr')`
* `"PRN_ShowEvents"` -> Show events for every function with `DebugFunctionIfEnabled` decorator
* `"BOL_HNDLE_DBGLST"` Handle debug list?
* `"SHW_OUTPUT"` Show output `(Do not execute functions marked with ExecuteIfEnabled("SHW_OUTPUT") decorator)`
* `"INTERP_EXEC_EVEN_IF_ERROR"` Execute even If there is a problem with command line arguments or current_line
* `"INTERP_EXEC_EVEN_IF_RAISED"` Do not Raise error If there was an error with command execution (`True = Do not raise error, False = Raise error`)
