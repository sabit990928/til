For all the Elixir lovers, here is a really cool function I found about recently - https://hexdocs.pm/elixir/1.13/Kernel.html#binding/1Where I find this really useful is calling it at the top of the function like so:

```elixir
def foo(a, b, c) do
  IO.inspect(binding())
  ...
end
```

It returns values of a, b and c as a keyword list

A concrete example, I have this function:

```elixir
  defp date_time_from_params(
         %{
           "start_time" => start_time,
           "end_time" => end_time,
           "start_date" => start_date,
           "end_date" => end_date
         } = _params
       ) do
    IO.inspect(binding())
    ...
  end
```

and in the console I get:

```elixir
iex(2)> [
  _params: %{
    "end_date" => "2022-07-20",
    "end_time" => %{"hour" => "8", "minute" => "20"},
    "event" => "Some event 1",
    "pay_type" => "Nurse",
    "start_date" => "2022-07-20",
    "start_time" => %{"hour" => "8", "minute" => "15"},
    "variant" => "Standard"
  },
  end_date: "2022-07-20",
  end_time: %{"hour" => "8", "minute" => "20"},
  start_date: "2022-07-20",
  start_time: %{"hour" => "8", "minute" => "15"}
]
```
