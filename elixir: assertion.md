For assert capture, you can use regex's or the =~ operator to match on the subset of the log that you care about:

```elixir

logs = ExUnit.capture_log(fn -> MyFun.call() end)
assert logs =~ "This is my Log. There are many like it but this one is mine."


```
