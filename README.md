# occ
*occ: the overcomplicated compiler*

Build tools saves time for the programmer but are not strictly necessary.
They are therfore always going to be adding unnecessary complexity by
definition that could easily blow out of proportion. The goal of occ is to
be as useful as possible while being mindful of complexity. Occ rejects the
makefile design, to have a turing complete language (script) with build
instructions. Instead occ relies on standardized occ.project files in JSON
format and tracks your installed projects for you.

## Quick Start

- `occ.project` specifies the build config for a project. See [librcd's](https://github.com/jumpstarter-io/librcd/blob/master/occ.project) for an example.
- `src/` contains source code, `include/` exported headers, and `libs/` external libraries with their own build scripts.
- `occ -x` will index the current directory as a project with the same name as the directory. The name is global, and used for dependency management.
- `occ -c -m <target>` will build a particular target (specified in occ.project), often "debug" or "release".
- Preprocessor and object file caches are stored in `~/.config/occ/`. `occ -cc`/`-cd`/`-ch` will clean them.
- Run `occ -h` to see all available flags.
