# Retrieve character codepoint

Lil intro. Lists in Elixir are effectively linked lists, which means they are internally represented in pairs containing the head and the tail of a list:
```elixir
  iex> [head | tail] = [1, 2, 3]
  iex> head
  1
  iex> tail
  [2, 3]
```

Verstehen? Yesterday I found out that we could implement such behavior for strings. It works as usual pattern matching: `<<first::utf8, rest::binary>> = "example"`, where `first` will be code point which value you can retrieve as `<<first>>` and `rest` is just the binary with value as `xapmle`. 