---
description: undefined vs undeclared vs uninitialized (aka TDZ).
---

# Kinds of emptiness

In English, they kinda are the same, but in programming, they are not (Especially in JS).

Undeclared means: It has never been created in any scope that we have access to.

Undefined means: There's definitely a variable and at the moment, it has no value. (This is the only type that is able to reference a thing that doesn't exist and does not throw an error.)

Uninitialized means: They never get set to undefined. when it's in an uninitialized state, it's off-limits, you are not allowed to touch it.

