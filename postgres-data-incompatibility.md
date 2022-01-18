# Postgres 13 -> 14 data incompatibility

_Background_: recently I have updated some local libraries. `postgres` was part of it too. Then I faced a problem when `postgres` couldn't connect to server. 

It showed such an error message. "The data directory was initialized by PostgreSQL version 13, which is not compatible with this version 14.1."

I tried to migrate my data from version 13 to 14 first. Community recommended such a solution:
```
rm /opt/homebrew/var/postgres/postmaster.pid
brew services restart postgresql
```
It didn't work for me because there's no such `postmaster.pid` file. 

Then I decided to simply remove local data by running:
```
postgres -D /opt/homebrew/var/postgres
```
It resets all to default and superusers needed too:
```
/opt/homebrew/bin/createuser -s postgres
```
