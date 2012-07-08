# Project: Programming language
## What's this?
This is my programming language playground. I want to design a new language, that is easy to use, but also as powerful as established languages like C#, Python, Ruby, and so on. I like minimal and expressive syntax, but it should stay readable, so Lispy-syntax must stay out. 

I want this to be the blueprint of a new programming language I want to design. I'll describe the key properties here in this document. Feel free to change or enhance this and send pull requests.

# Functions
## Definition:
At first, a function is like every other piece of code, but it has some special properties:
+ A name
+ parameters (optional)
+ A return type (if no explicit return type was specified, it is nil)
+ scope (every variable declared in a function is only visible in the function)
+ Can be assigned to a variable
# Variables
## Definition
A variable is a named piece of memory, that can hold a reference on:
+ a value (int, float, string, character, boolean)
+ an instance of a class
+ a function
A variable is immutable by default, it must be prefixed with **mutable** if you want to change its value later on.
It must be prefixed with **local** if you want to keep it in the current scope only. Otherwise, it is visible in the current scope and all nested.




Created with iA Writer.
