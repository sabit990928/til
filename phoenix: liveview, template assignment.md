Seems like you can call specific template that way as well:

```elixir
def handle_info("do_full_details", socket) do
  socket
  |> assign(:template, "full_details")
  |> noreply()
end
```
