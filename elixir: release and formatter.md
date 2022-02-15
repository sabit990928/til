# Elixir release, heex formatter, dependabot

1.13.3 version was released recently. Contains several bugfixes and enhancements related to `mix format`, now it supplies file, line to formatter plugins and support embedded Elixir expressions inside formatter plugins.

It doesn't contain formatting for `.heex` files(templates), but recently I heard about [heex_formatter](https://github.com/feliperenan/heex_formatter) package which can do that job for you.
We doing formatting manually and it's not a big problem actually.

---

Dependabot can make pull request when some of your repo dependencies update it's version. Previously it just sent me some emails or just notified in github. Actually I don't know how to configure it, but it's pretty helpful feature. Yeah your branches and pull request could stay messy some time if you ignoring pr recommendations.
