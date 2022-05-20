# Forth-in-Charm
An implementation of Forth in the Charm scripting language.

I’ve followed the spec for Forth I found on this webpage. https://skilldrick.github.io/easyforth/ , except for keyboard input.

ex backtick <forth code> backtick will execute the given code.

You should use backtick quotes so you don’t have to escape " for Forth.

show followed by either code, stack, mem, vars, consts, defs, output, error, and loopVar will show the relevant aspect of the state of the Forth machine: show all will show all the fields.

Similarly clear followed by any of those things will set it to its original state, and clearall will reset the Forth machine entirely.

Note 1 : show code will only return a non-empty list if execution has failed with an error, in which case it will contain the unexecuted code.

Note 3 : similarly show loopVar will always return NIL: it has an integer value only during the execution of a loop.

Note 3 : clear defs will still leave the built in definitions of ? and +!
