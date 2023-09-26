### Tuple

Tuples are often used in Elixir for memory read-intensive operations, since read-access of an element is a constant-time operation. They are not usually used when elements may need to be added/removed dynamically because rather than modifying the existing tuple, a new tuple is created which requires memory to be allocated upfront.

Elements in a tuple can be individually accessed using the elem/2 function using 0-based indexing:

```elixir
empty_tuple = {}
one_element_tuple = {1}
multiple_element_tuple = {1, :a, "hello"}

elem(multiple_element_tuple, 2)
# => "hello"
```

_FYI_
Any variable starting with an `_` is not tracked by the runtime.
