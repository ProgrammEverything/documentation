---
layout: default
title: "How does it work?"
parent: "Sarvar"
nav_order: 2
---

## How does it work?
Engine(`cmd: dict[str, EngineCommandFunction]`, `logger: Logger = Logger()`)\
`cmd` keyword argument: `List of all commands`
* Structure
  - `{"Command": Callable of type EngineCommandFunction}`
Each Command function is defined by the `@Engine.engine_command decorator factory`
* Each function gets these arguments
    - `CommandFunction(token: Token)`\
Example:
```python
@Engine.engine_command(bigger_than=0, lesser_than=float("inf"), macro_immutable=False)
def printContent(token: Token) :
    token.args.append("Print")
    token.args.append(" ".join(token.privatevars))