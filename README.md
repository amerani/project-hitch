# project-hitch

This repository consists of git submodules for various components of the project that are in their own repos, and tooling required to develop locally and deploy to production.

## Manage changesets

#### Setup local copy

`git clone --recurse-submodules git@github.com:amerani/project-hitch.git`

`git submodule foreach 'git checkout master'`

#### Fetch changes from remotes without local changes

`git submodule update --remote`

#### Merge remote changes with local changes

`git submodule update --remote --merge`

#### Rebase local changes onto remote changes

`git submodule update --remote --rebase`

## Bootstrap development environment

`.env hitch-api/.env hitch-web/.env`

```
PG_HOST=db
PG_PORT=5432
PG_USERNAME=postgres
PG_DATABASE=hitch_app
API_PORT=8080
```

`docker-compose up`

* api-docs - http://localhost:8080/graphiql
* api - http://localhost:8080/graphql
* web ui - http://localhost:3000
