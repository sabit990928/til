# GenServer functions

Refreshed knowledge about GenServer. Elixir related stuff. It's a behavior module for implementing the server of a client-server relation. It will also fit into a supervision tree.

To handle synchronous requests we need to implement the `GenServer.handle_call/3`.

Asynchronous requests are handled with the `handle_cast/2` callback. 

`handle_info/?` fetches everything else that does not fit in for `handle_call` and `handle_cast`.

[Link](https://elixirschool.com/en/lessons/advanced/otp_concurrency) for example.