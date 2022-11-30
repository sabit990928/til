It does not make any diff.

```elixir
defmodule Test do
  def one(socket = %{assigns: %{hello: :world}}), do: socket
  def two(%{assigns: %{hello: :world}} = socket), do: socket
end

iex(32)> socket = %{assigns: %{hello: :world, bonjour: :monde}, pid: 1}
%{assigns: %{bonjour: :monde, hello: :world}, pid: 1}
iex(33)> Test.one(socket) == socket
true
iex(34)> Test.two(socket) == socket
true
iex(35)>
```

Wow. I didn't know that. Thought first way is kinda wrong way. One of my teammates shared it.
