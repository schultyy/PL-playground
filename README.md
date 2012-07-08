# Project: Create a new programming language
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
A function can call itself, known as **recursion**. This can lead to more memory consumption, but it is quite useful in some scenarios. The recursion limit is **undefined at the moment**. 
# Variables
## Definition
A variable is a named piece of memory, that can hold a reference on:
+ a value (int, float, string, character, boolean)
+ an instance of a class
+ a function
A variable is immutable by default, it must be prefixed with **mutable** if you want to change its value later on.
It must be annotated with **local** if you want to keep it in the current scope only. Otherwise, it is visible in the current scope and all nested.

# Scope
## Definition
A scope defines a protected area where variables and functions are stored. A new scope is created by one of the following keywords(…) and ends with **end**.
A scope can contain other scopes. All items in the current scope are visible in nested scopes, excluding those variables with are marked as **local**.

# Paradigms
## Functional
At first, some basic features should be supported, like pass a function as parameter to another function, assign a function to a variable and so on. Also immutable variables are important.
## Class based
I like JavaScript's prototype approach, but classes seem to fit better for the daily business.
## Future
### Aspects
Some languages and libraries provide 'Aspect functionality'. It is very helpful, to annotate pieces of code with a feature, that is commonly used in the whole project, but if just implemented at those places in the old fashioned way, the code gets very messy.
## …
# Code examples
## Disclaimer
This is a first draft of how code *could* look like. So don't expect stable stuff.

## Comments
// I am a classic C-Style comment
--
	I am a multiline comment
--
## Define a function:

	function Foo()
		bla()
		bar()
	end
## Assignments:

	a = 5
	b = "This is a string"
	pi = 3.14

## Conditionals:

	if foo() then
		bar()
	else
		baz()
	end

### Selection control
#### Description
Most programming languages have a construct like **switch**, **select case** or something like that. I like those, because it is a nice and fast way to define cases. But until today I miss a certain feature:
Define all cases with their specific stuff *and* the code which is equal for some or all cases.

	switch(foo)
		case A:
			//specific stuff for case 'A'
		case B:
			//specific stuff for case 'B'
		case C:
			//specific stuff for case 'C'
		case D:
		 //specific stuff for case 'D'
		common(A,B):
		//Common code for 'A' *and* 'B'
	end
