Dialyzer Ignore
You can create such file: `.dialyzer_ignore.exs` in root folder(I guess) and dialyzer will ignore containing files for warning messages.

```elixir
[
  # {file}
  # following to this https://github.com/phenixdigital/phx_live_storybook/issues/132 thread
  # the issue is known but not to be addressed (at least for now, hopefully)
  {"lib/backend_web/storybook.ex"}
]
```
