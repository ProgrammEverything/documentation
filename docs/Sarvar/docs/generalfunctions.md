---
layout: default
title: "General functions and instance setup"
parent: "Sarvar"
nav_order: 6
---
### General functions and instance setup
To setup an instance first import the "Sarvar" package
```python
>>> import Sarvar as sr
>>> # Then make an instance by the following structure: Engine (cmd: dict[str, EngineCommandFunction], logger: Logger = Logger() #Optional# )
>>> myInstance = sr.Engine({}) # Meaning no commands by default
```