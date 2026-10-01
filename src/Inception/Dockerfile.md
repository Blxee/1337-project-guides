# Commands:

### `FROM`

Start from a base image, pull it from docker hub or use the local cached version if it exists.

#### Formats:

* `FROM <image>`
* `FROM <image>[:tag]`
* `FROM <image>[@digest]`

`image` is the image name to be used (pulled from docker or uses local cached one).
`tag` is the version or the name of the version, (`latest` is the default).
`digest` a unique _sha-256_ hash to identify an exact image.
#### Examples:



> Note: the `FROM` command **must be the first non-comment line** in a dockerfile, and only be called once.

---
### `RUN`

Run a command **when building the image** from the dockerfile.
Use this command for installing dependencies or commands that change the file system.

#### Formats:

* `RUN <command> [arg1] [arg2] ..`
* `RUN ["<command>"[, "arg1"][, "arg2"] ..]`



| command | description                                                                                                     | constraints | formats  | arguments                                                                                  | example                                       |
| ------- | --------------------------------------------------------------------------------------------------------------- | ----------- | -------- | ------------------------------------------------------------------------------------------ | --------------------------------------------- |
| `RUN`   | run commands when building the image, these are commands that change the file system and only need to run once. | N/a         | <br><br> | `command` is the command to run when building followed by any number of optional arguments | <br><br>`RUN ["apt-get", "install", "nginx"]` |
