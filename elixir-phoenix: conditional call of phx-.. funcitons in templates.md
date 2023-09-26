### Conditional call of phx-... functions in templates

Here's the story. We updated our elixir, phoenix and liveview versions from:

```
  {:phoenix, "~> 1.6.6"},
  {:phoenix_live_view, "0.17.7"},
  elixir: "~> 1.5",
```

to

```
  {:phoenix, "~> 1.7.6"},
  {:phoenix_live_view, "0.19.3"},
  elixir: "~> 1.15",
```

Below syntax in the template worked fine with old version

```
<td
  class={if type in [:integer, :decimal, :precise, :percent], do: "text-center"}
  {if column in @clickable_columns, do: [phx_click: "drill_down", phx_value_row: row_index, phx_value_column: column, phx_target: "##{@id}"], else: []}
>
```

It somehow converted `phx_click` atom value to `phx-click` on fly, while with new version you can't write it in such a way.

So we rewrote it like so:

```
<td
  class={if type in [:integer, :decimal, :precise, :percent], do: "text-center"}
  {if column in @clickable_columns, do: ["phx-click": "drill_down", "phx-value-row": row_index, "phx-value-column": column, "phx-target": "##{@id}"], else: []}
>
```

were we're passing functions in such a way: `"phx-click":`
