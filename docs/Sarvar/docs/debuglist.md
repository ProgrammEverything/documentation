---
layout: default
title: "Debug list"
parent: "Sarvar"
nav_order: 5
---
### Debug list
Commands:
```python
{
    "Warn": self._warn_attr,
    "Error": self._error_attr,
    "Debug": self._debug_attr,
    "Print": self._print_attr,
    "MakeCall": self._make_call_attr,
}
```
Insert a command or key into the `token.args` list to be handeled in the `_handle_debug_list` function
- Structure
  * `["Command-Key from commands", "Arguments for the specified commands"]`
  * Example:
    - ["Warn", "hello!", "Error", "This"]
    - Executes "Warn" function from dict with arguments - argument `"hello!"`
    - Executes "Error" function from dict with arguments - argument `"This"`