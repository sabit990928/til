# Fundamentals

Refreshed knowledge related to Elixir by making exercises from [Exercism](https://exercism.org/).
There are some notes from it: 
- Elixir actually compiles down to bytecode and then runs on the BEAM Erlang Virtual Machine.
- Being a functional language, everything in Elixir is an expression.
- Programmers use Elixir to handle thousands of requests and responses concurrently on a single server node.
- All data in Elixir is immutable, allowing for safer and easier-to-reason-about concurrency.
- Dynamically typed. Elixir has no compile-time type checks, favoring run-time pattern matching. Elixir is a dynamically-typed language, meaning that the type of a variable is only checked at runtime. Using the match = operator, we can bind a value of any type to a variable name.
- All modules are available to all other modules at runtime and do not require an access modifier to make them visible to other parts of the program.

HashMap analogue - `Enum.with_indexes\2`

# Other
Leethub is useful tool where you can commit exercise to repo when click submit button. But it seems like commit messages named with heavy text: speed, memory, etc. Each task as a folder with description file and solution file. 
I decided to keep it simple. Just created private repo with manual commit, pushes on it. There's no problem description, but I think the main purpose about keeping name of the problem to have quick reference in Leetcode.