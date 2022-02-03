# Constants

There are 2 ways to create constants/global variables in Elixir:
- by creating a Module attribute
- with help of metaprogramming(Uhhhh)

Module attribute value exists only during compilation time. Also it can't be accessed outside the module in which it's declared.

By creating abstract layer function to return constant value. This approach uses macros and it's accessible outside of the declared module. More details [here](https://blog.kiprosh.com/constant-in-elixir/).
