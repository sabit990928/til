### Multiple Clause Functions

_All below are notes from exercism. (Main stuff, but not all to be fair)._

Elixir facilitates **Open-Closed Principle** practices by allowing functions to have multiple clauses, so instead of sprawling and hard-coded control-logic, pointed functions can be written to add/remove behavior easily.

At **run-time**, Elixir will test, from top to bottom of the source file, which function clause to invoke.

### Guard

Guard functions are special functions which must be pure and not mutate any global states.

### Default arguments (\\)

```elixir
# Example
def number(n \\ 13), do: "That's not my favorite"
```

When compiled, Elixir creates a function definition for `number/0` (no arguments), and `number/1` (one argument).

If more than one argument has default values, the default values will be applied to the function from left to right to fill in for missing arguments.
(I'm not sure that I understood above paragraph. Maybe I'm stupid, but usually default value stays near attribute. So I checked my theory. Heh)

```elixir
iex(1)> defmodule Cmon do
...(1)> def a(aa \\ 5, b \\ 4), do: aa + b
...(1)> end
{:module, Cmon,
 <<70, 79, 82, 49, 0, 0, 6, 100, 66, 69, 65, 77, 65, 116, 85, 56, 0, 0, 0,
   155, 0, 0, 0, 16, 11, 69, 108, 105, 120, 105, 114, 46, 67, 109, 111,
   110, 8, 95, 95, 105, 110, 102, 111, 95, 95, 10, 97, ...>>, {:a, 2}}
iex(2)> Cmon.a
9
iex(3)> defmodule Cmon do
...(3)> def a(aa, b \\ 4 99), do: aa + b
...(3)> end
** (SyntaxError) iex:4:18: syntax error before: "99"
    |
  4 | def a(aa, b \\ 4 99), do: aa + b
    |                  ^

iex(3)>
```

If the function has more than one clause, the default arguments should be defined in a function header (a function without a body) before the function clauses:

```elixir
def number(n \\ 13)
def number(n) when n < 10, do: "Dream bigger!"
def number(n) when n > 100, do: "Not that big..."
```

p.s. above kinda obvious things, but it's good from time to time refresh that knowledge. e.g. I frequently forget about sign for default argument. Like was it // or \\.
