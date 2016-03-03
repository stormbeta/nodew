#nodew

Simple wrapper around `nvm`.

Features:

* Sourceable
* Works even if nvm isn't installed on the system
* Includes project-local utilities (via `node_modules/.bin`)
* Sourcing from another project unloads the previous project automatically
* Can be used as a direct command wrapper, not just sourced

##Usage

Put `nodew` in your project, and simply source it to setup your project's node environment (defaults to current Node LTS version).

* Uses `.nvmrc` if present (or `NODE_VERSION` if set) to select project's node.js version, just like `nvm`

* Injects `node_modules/.bin` into your `PATH` if `package.json` is found

* `./nodew COMMAND` will run against the project's node environment without sourcing it into your shell

##Future

* Planned to integrate with the ReadyTalk [Gradle JS plugin]

* Windows support?
  -> it's possible to create a single polyglot script
     but nvm doesn't support windows, so we'd need to pull something else in
     or manage the download and installation directly

[Gradle JS Plugin]: https://github.com/ReadyTalk/gradle-ReadyTalk-js
