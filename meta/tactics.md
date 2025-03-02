# Tactics

Tricks that I might use in order to make things work, in the Golang version or otherwise.

> Input structs

If you want to be able to leave some inputs to a function as nil, maybe inputting them as fields in a single struct will allow less verbose calls.

> No '=' assignment

Requiring `new(...)` constructors which are capable of returning nil or error could allow for certain patterns.

> Function parameter affixes

In Nyo code, perfixing function params `doSomething(_err, x_, ~y~, ~z#)` could enforce certain behaviors.

Possibilities:
- Must be `_undefined` before call
- Must be `undefined_` on return
- Must be `~defined` before call
- Must be `defined~` on return
- Must be `unmodifiable#` by function (read only)
- Must be `?unreadable` by function (write only)

> Struct field affixes

Similar treatment might be given to struct fields.