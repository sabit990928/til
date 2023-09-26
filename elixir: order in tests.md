`assert_unordered_list_equality`

One thing to note is that tests within a test file always run synchronously. If the file is marked to run async, the module might run at the same time that another module of tests runs. So, if you really need to have some synchronous tests, you can put them in their own module (in the same file). That allows most of the tests to run async:

```elixir
defmodule MyTest do
  use ExUnit.Case, async: true

  test "my_fun/3" do
    ...
  end
end

defmodule MySynchronousTest do
  @moduledoc "These tests are synchronous because blah blah..."
  use ExUnit.Case, async: false

  describe "my_fun/2" do
    ...
  end
end
```

Here is a summary of what you should avoid doing, for easy reference:

- Don't use Application.put_env in async tests.
- Don't use :shared mode on the Ecto sql sandbox in async tests.
- Ensure unique data is unique across all tesqtsq.
- Never rely on the order of logs in a test.
- Consider mocking ETS/:persistent_term for testing.
- If you rely on database order, specify it.
- Mock dates, times, datetimes, and random.
- Prefer assert_receive/3 over assert_received/2
