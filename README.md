# heroku-buildpack-yarn-workspaces

This buildpack is intended to allow a monorepo using yarn workspaces to build and run the specified workspace as the main Heroku app.

```
heroku buildpacks:set --index 1 "heroku/node" -a yourappname
heroku buildpacks:add "https://github.com/blockhq/heroku-buildpack-yarn-workspaces#master" -a yourappname
heroku buildpacks:add "heroku/ruby" -a yourappname # if need a different buildpack to run your app
heroku config:set APP_ROOT="path/to/workspace" -a yourappname

```

It is meant to be used in conjunction with the node buildpack first, followed by whatever buildpack is needed to run your app.
