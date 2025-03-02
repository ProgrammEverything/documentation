---
layout: default
title: "Logger class"
parent: "Sarvar"
nav_order: 7
---
#### Logger class
    Logger class is a class designed for outputing "Engine" outputs
    Such as 'Errors-Warnings and ...'
    How to setup class:
        def_debug = stdout, def_warn = stderr, def_print = stdout, def_err = stderr
        Your output files such as stdout - stderr - ...
        Prints using rich into specified files by specific functions
            def log_error(self, it): rich.print("[red]"+ "ERROR:\t" +str(it)+"[/red]", file=self.error_file)
            def log_warning(self, it): rich.print("[yellow]" + "WARNING:\t" +str(it)+"[/yellow]", file=self.warn_file)
            def log_debug(self, it): rich.print("[blue]"+ "DEBUG:\t" + str(it)+"[/blue]", file=self.debug_file)
            def log_print(self, it): rich.print("[cyan]OUTPUT:\t"+str(it)+"[/cyan]", file =self.print_file)

* `add_cmd` -> Adds a new command `(Args: str, callable)`

* `remove_cmd` -> Removes a command `(Args: str)`

* `push_to_stack` -> Pushes a command to execution stack (`self.commands`) and adds one to the len of execution stack (`self.all_lines`) `(Args: str)`

* `interpret` -> interprets the current line (`self.current_line`) `(Args: None)`

* `HELPER_InterepetAll` -> interprets until the current line becomes bigger or equal than all of the lines (`self.current_line < self.all_lines`) `(Args: None)`

* `set_flag` -> Sets a specific flag to the specified value `(Args: str, bool)`

* `unset_flag` -> Unsets a specific flag `(like the 'not' keyword)` `(Args: str)`

* `Flags` -> `[PROPERTY]` Returns the `self.readView`

* `get_cmd` -> `[PROPERTY]` Returns the `self.cmd` dictionary
