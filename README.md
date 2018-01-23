# nodew

Simple wrapper around `nvm`.

Features:

* Sourceable
* Works even if nvm isn't installed on the system
* Includes project-local utilities (via `node_modules/.bin`)
* Sourcing from another project unloads the previous project automatically
* Can be used as a direct command wrapper, not just sourced
* Uses latest LTS release of node by default

## Usage

Put `nodew` in your project, and simply source it to setup your project's node environment (defaults to current Node LTS version).

* Uses `.nvmrc` if present (or `NODE_VERSION` if set) to select project's node.js version, just like `nvm`

* Injects `node_modules/.bin` into your `PATH` if `package.json` or `package-lock.json` are found

* `./nodew COMMAND` will run against the project's node environment without sourcing it into your shell

* `./nodew` will prompt you to update the script to the current master from this repository

## Future

* Windows support?
  -> it's possible to create a single polyglot script
     but nvm doesn't support windows, so we'd need to pull something else in
     or manage the download and installation directly
