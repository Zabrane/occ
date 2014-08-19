# occ
*occ: the overcomplicated compiler*

Build tools saves time for the programmer but are not strictly necessary.
They are therfore always going to be adding unnecessary complexity by
definition that could easily blow out of proportion. The goal of occ is to
be as useful as possible while being mindful of complexity. Occ rejects the
makefile design, to have a turing complete language (script) with build
instructions. Instead occ relies on standardized occ.project files in JSON
format and tracks your installed projects for you.
