### List

Elixir implements lists as a linked list, where each node stores two values: the first item and another list with all the remaining items.

```elixir
# [1] represented in [head | tail] notation
[1 | []]

# [1, 2, 3] represented in [head | tail] notation
[1 | [2 | [3 | []]]]
```

We can use [head | tail] notation to prepend elements to a list:

```elixir
# Suppose
list = [2, 1]

[3, 2, 1] == [3 | list]
# => true
```

Lists in Elixir are implemented as linked lists, and not as arrays of contiguous memory location. Therefore, accessing an element in a list takes linear time depending on the length of the list.

<!-- Linear time, it's not telling me anything. O(n) I guess -->

```elixir
# Multiple prepends
[1, 2, 3 | [4, 5]]

# Appending to the end of a list (potentially slow)
[1, 2, 3] ++ [4] ++ [5] ++ [6]

# Prepend to the start of a list (faster, due to the nature of linked lists)
[6 | [5 | [4 | [3, 2, 1]]]] # then reverse!
```

There are several common Kernel functions for lists:

- hd/1 returns the head of a list -- the first item in a list.
- tl/1 returns the tail of the list -- the list minus the first item.
- length/1 returns the number items in the list.
- in/2 returns a boolean value indicating whether the item is an element in the list.
