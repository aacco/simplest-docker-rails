# The simplest Docker container for Rails7
## Set up
```
docker compose build
docker compose run --no-deps web rails new .
docker compose up
```
or you can type instead of line 2:
```
docker compose run --no-deps web rails new . --force --database=postgresql
```
And you finish:
```
docker compose run web rake db:create
```

## Exec ruby container
```
docker exec -it rb-web bash
```

# if you get ERRORs...
## exec /usr/bin/entrypoint.sh: no such file or directory
if you get
```
exec /usr/bin/entrypoint.sh: no such file or directory
```
when you exe:
```
docker compose run --no-deps web rails new .
```
make sure `entrypoint.sh` uses `LF`, not `CRLF`.
