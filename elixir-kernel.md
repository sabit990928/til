# Kernel

Kernel is Elixir's default environment. It consists of:
- basic language primitives, such as arithmetic operators, spawning of processes, data type handling, and others. 
- macros for control-flow and defining new functionality (modules, functions, and the like).
- guard checks for augmenting pattern matching.

All of its functions automatically imported into Elixir code. Usually I never thought about how addition, subtraction operators work. I mean, in any environment. It seemed like built in stuff under the hood, I haven't researched for other languages, but here you can write something like `Kernel.+(5, 8)`. It's not a game changer, it won't affect to how you write code, but at least it's fun thing to know.