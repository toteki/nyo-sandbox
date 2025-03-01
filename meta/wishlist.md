# Wishlist

Documenting possible goals for the Nyo language.

Mutually exclusive or incoherent goals are allowed.

> Anything in Nyo can be undefined.

- All types can be nil
- Index out of range returns nil
- Method calls on nil are no-ops

> Nyo can enforce defined inputs and outputs at compile-time

If a function can have an undefined result, compiler must stop it from feeding into a function whose input must be defined.

Broadly, the compiler must be able to track the possible states of all variables.

> Nyo programs cannot panic.

Requires recovery from some classes of error, like out of memory. Others, like nil stuff, can be more graceful.

> Nyo outputs Go libraries, not programs.

This would be a transpiler approach.
- Allows stricter rules on what Nyo makes
- Allows integration with Go programs (which may use Go features or standard library)
- Nyo outputs may actually be useful

> Nyo outputs libraries in multiple languages.

Extends transpiler approach. Complicates everything, everywhere.