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