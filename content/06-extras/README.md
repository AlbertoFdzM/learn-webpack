# Extras

## A PRETTIER OUTPUT

If the project grows the compilation may take a bit longer. So we want to display some kind of progress bar. And we want colors…

We can achieve this with:
```bash
webpack --progress --colors
```

## WATCH MODE
We don’t want to manually recompile after every change…
```bash
webpack --progress --colors --watch
```

Webpack can cache unchanged modules and output files between compilations.

When using watch mode, webpack installs file watchers to all files, which were used in the compilation process. If any change is detected, it’ll run the compilation again. When caching is enabled, webpack keeps each module in memory and will reuse it if it isn’t changed.

## DEVELOPMENT SERVER

The development server is even better.
```bash
npm install webpack-dev-server -g
```
```bash
webpack-dev-server --progress --colors
```

This binds a small express server on localhost:8080 which serves your static assets as well as the bundle (compiled automatically). It automatically updates the browser page when a bundle is recompiled (SockJS). Open http://localhost:8080/webpack-dev-server/bundle in your browser.

The dev server uses webpack’s watch mode. It also prevents webpack from emitting the resulting files to disk. Instead it keeps and serves the resulting files from memory.
