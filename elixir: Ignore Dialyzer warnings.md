### Ignore Dialyzer warnings

You can create any file in root folder, let's call it `.dialyzer_ignore.exs` and dialyzer will ignore containing files for warning messages.

Example of what's inside the file:

```elixir
[
  # {file}
  # following to this https://github.com/phenixdigital/phx_live_storybook/issues/132 thread
  # the issue is known but not to be addressed (at least for now, hopefully)
  {"lib/backend_web/storybook.ex"}
]
```

Then you need to update your dialyzer details in `mix.exs` like below:

```elixir
dialyzer: [
  plt_file: {:no_warn, "priv/plts/dialyzer.plt"},
  ignore_warnings: ".dialyzer_ignore.exs"
]
```
