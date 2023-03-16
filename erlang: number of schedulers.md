### BEAM's number of started schedulers

By default, BEAM starts a scheduler for each (logical) CPU core available. You can check the number of schedulers that BEAM has started with :erlang.system_info/1:

```elixir
iex> :erlang.system_info(:schedulers_online)
8
```
