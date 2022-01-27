# List appending vs prepending

Due to their cons cell based representation, prepending an element to a list is always fast (constant time), while appending becomes slower as the list grows in size (linear time):

```elixir
iex> list = [1, 2, 3]

iex> [0 | list] # fast
[0, 1, 2, 3]

iex> list ++ [4] # slow
[1, 2, 3, 4]
```