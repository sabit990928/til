# Oban's date props

It's about specific case. [Oban](https://hexdocs.pm/oban/Oban.html) is a robust job processing library which uses PostgreSQL for storage and coordination.
When you create new event, it passes params to `perform/1` which executes the job, **but** it converts utc datetime(`~U[2022-02-21 10:45:00Z]`) to iso8601(`"2022-02-21T10:20:00Z"`). I don't know what's the reason. It was the cause of one bug in my case.
