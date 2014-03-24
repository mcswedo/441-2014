# Questions taken from http://csusbdt.github.io/441-2014/lua.html

# Section 1
- "Clean C" is defined as the common subset of Standard C and C++, in other words, will
compile and run on both a C compiler and a C++ compiler with no noticeable errors.
- The host is written in C.
- The LUA executable uses the LUA library to give a standalone LUA interpreter to the user.
This allows command-line interactive or batch (file input) usage.

# Section 2
- Dynamically typed means that variables do not have types - only values do.
- The eight basic types in LUA are: nil, boolean, number, string, function, userdata,
thread, and table.
- One, the value 'nil' itself. Meant to be different from all other types.
_question might not be needed, perhaps replace with a programming question_
- Two, true and false (or nil)
- Double-precision floating point, or double.
- Immutable means that the state of the sequence of bytes cannot be changed after creation.
- Any byte value, including embedded zeroes.
- _PERHAPS A QUESTION HERE ABOUT TYPES OF VARIABLES - INITIALIZE A BOOL, CHANGE TO INT, TO NUMBER, TO STRING_
- Assignment and Identity Test.
- No, Lua threads are not threads from the operating system - they are coroutines
usable on any system.
- The values not allowed as keys are nil and NaN. The value not allowed in the table is nil. 

# Section 2.2

- The variable _G refers to a global variable. 
- Input into the INTERPRETER, this program prints 1, 1, 1, 1. 
I believe the local keyword used here will not work - the line local x = 2 needs to be
_ENV.x = 2 if it is used in the interpreter. Used as a file test.lua, however, it works.

# Section 2.3

- Catching errors can use either the pcall or xpcall to call a function in a protected mode.

- Explicitly generating an error can be done by calling the error function.

# Section 2.4

- Tables do NOT have metatables by default.

- Haven't done it yet.

# Section 2.6

- An operating system thread is automatically started and stopped, and is, conceptually, a
form of concurrent processing - multiple operations being handled at the same time.
A coroutine is a called function that is completed in sequential order and then passes
back to its caller.