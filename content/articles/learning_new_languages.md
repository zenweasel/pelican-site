Title: Learning New Languages
Date: 2015-08-15
Category: Articles

### Introduction

For reasons of both chance and choice I have had to learn several new programming language in a relatively short time. I have definitely not become an expert in any of them, but I have learned how to get things done. I would probably lose a programming quiz about the ins and outs of these languages, but I have a lot of working, quality code out in the wild in those languages.

So based on this experience I have decided to try to summarize what I have found the most important things to learn to be productive. More than once I have sat down and tried to \"learn the language\" from the beginning and just been overwhelmed with trying to cram a lot of new concepts into my head. So now I take this approach and it has been less painful and more fun.

**50,000 ft view steps**

*   If applicable learn which types of applications language is targeted at. e.g. Node is not really targeted at Desktop GUI applications. Objective C not really targeted at Enterprise Web apps. Understand if you may have a round peg in a square hole, and once you have enough knowledge, say so.

*   Figure out if the language you are learning has a vastly different paradigm than the ones you know, e.g. if you are a Java programming and you are learning Python, much of the high-level concepts will be the same. However if you are learning Erlang or Haskell you will need to drop most assumptions you have (for example in Erlang all variables are immutable and there is no real \"if\" statement). I cover this in \"Language Design\", but its good to know up front how much unlearning you will be doing.

#### Data Types

**Learn common data types (ones that fit well known structures, e.g. array, hashmap, etc)**

I am of the opinion that often a lot of what you end up doing from day-to-day is converting data from one type to another, or storing or retrieving data from a type. This tends to give you a big advantage at first and also gives you a taste on how similar the language is to the ones you know.

**For each data type:**

*   Create
*   Use
*   Convert to other known data types
*   Any gotchas in terms of operations on data types

*   **Learn specialized data types (ones specific to the language)**
    *   Understand the cases where these are needed/used
    *   Convert to/from common data types

### Infrastructure

**Learn how to set up a productive development environment, and how to discover and manage code that's already been written for you**

*   Learn what package management system is available and if a sandboxed development environment is common practice. (Think rvm, virtualenv).

*   Learn how dependencies are handled

*   If the language has a \"standard library\" where that is, and how to quickly access documentation. Scan though library and see functions that you see yourself likely using and bookmark.

*   Discover what 3rd party package are in common usage. Especially ones that provide functionality in the area you are targeting, or provide an easier-to-use wrapper around a more difficult stdlib.

*   What build process tools are available.

### Language Design

**What sets this language apart from other languages, and how much does it deviate from the predominate C-syntax/Java Class inheritance paradigm.** _(not applicable if learning C or Java)_

*   Which parts of OO-programming does it implement if any: Encapsulation? Polymorphism? Inheritance? If Inheritance is supported, does it support Multiple Inheritance?

*   If it does not support a part of OO, what other methods does it use to solve those problems, if it does.

### Language Basics (the nitty gritty)

*   Typing/Comparisons.(Static/Dynamic) What implicit conversions does the language do to the different data types? What about operators? Does \"2\" * 12 = 24 or 2222222222222?

*   Does it use \"[duck typing](\"http://en.wikipedia.org/wiki/Duck_typing\")\" or similar?

*   If the language is static, how do you cast variables to different types and which types can't be cast to other types?

*   Can you create custom types and cast common types to/from these. (e.g. create your own version of a Hashmap and cast a normal Hashmap to this)

*   Conditionals (if/case/switch) If the language provides more than one form of if/then/else what are they?

*   Control/Looping structures: for, while, do/while. How do you break out of a loop (if you do) when a condition is met and you do not wish to continue?

*   How do you loop over a collection (e.g. forEach)

*   Variable scoping: Which types of scoped variables exist, global, module, function, class, etc. How do you specify scope? _(this item may really deserve to be part of language design)_How do you move values between different scopes? Pass by value or pass by reference?

*   What are the string functions (toLower, etc) and what formatting functions are available?

*   How is parameter passing done? Positional, named, both, neither?

*   Is there a constant or constants that represent \"null\"?

*   Which types can be serialized (to JSON etc) and how.

*   How does the language deal with Unicode?

*   Does the language support closures?

*   Does the language treat functions as first class citizens?

*   What flavor of regex does it use and how does it differ from PCRE?

*   Are variables mutable?

*   How do you handle Date formatting and date math.

*   Beyond the obvious what math operators are available and are they in the stdlib or the language itself?

*   How do you handle discovering/using file paths? When are relative paths ok, and how do you calculate absolute paths?

### More advanced language topics

*   How do you deal with \"blocking\" calls? Multi-threading (Java/Python), Asynchronous event loop (Javascript)?, spawn independent processes (Erlang), other?

*   What, if any, memory management tasks are required? How do you ensure that variables, etc. are released for Garbage Collection as soon as they are no longer used?

*   How does the language talk to Databases and other outside resources?

*   How does the language handle inter-process communication?

*   Does the language have an Event model? If so, how do you use it

### Building Programs

*   What is the proper way to handle exceptions

*   What debugging tools are available to you? From print() on up. Is there an interactive debugger where you can insert breakpoints, and if so how do you set it up?

*   If you are building a program that should execute from the command line or directly, what structure needs to be in place (e.g. main()?)

*   Is there an accepted style guide and are there any tools to help you follow these (e.g. PEP8 and PyLint, JSLint/JSHint)

*   What code quality tools are available that will help you catch obvious errors (if your IDE doesn't already do this for you).

*   What logging tools are available.

*   How do you do namespaces, or other equivalent ideas for code organization?

### Stage Two - Write a bunch of programs

Build these programs from scratch (not counting building them during running through tutorials, etc).

_(Please substitute your own name for mine)_

It's important that your write these programs from scratch and not find an example and cut and paste. While you can always look up syntax, you don't want to be doing that for the things you do 100 times an hour. Of course you will need to look things up, but try not to just copy (even by manually typing) what you find in the book.

For some language these won't make any sense, or they would be much more complicated than implied by the order. If so, just use your own judgement and come back to it, and just disregard it. Note that these go from very easy to very difficult, or at least more time-consuming, so expect that some of the later ones will take some time.

*   hello world
*   hello brent (input name)
*   hello if brent else world
*   hello brent printed x times
*   hello brent with min/max on name length, and friendly error message on over/underflow.
*   hello brent with bad input (e.g. non-alphanumeric) that outputs an error message
*   hello brent as a function
*   A Greeter class with a HelloBrent subclass
*   Instead of read/write to the console, have hellobrent read values from a file and output values to different file.
*   Build a function where one value may sometimes be a null.
*   Build a program that reads all the files from a directory and prints out the files in a readable format.
*   Write a program that accepts numbers input as 2,6,5,4,7,1,4 and will print them back sorted.
*   Write a program that accepts word input as word,word,word and print them back sorted.
*   Write an implementation of a [binary search tree](\"http://en.wikipedia.org/wiki/Binary_search_tree\").
*   Write an implementation of a [linked list](\"http://en.wikipedia.org/wiki/Linked_list\").
*   Build a program that will print the day of the week for any date in the future.
*   Build a program that simulates the roll of two six-sided die and prints their values.
*   Build a program that will print the fiboncacci series to infinity and never run out of memory.
*   Build a program that will parse a text file and give you the number of occurrences of a particular word.
*   Build a program that accepts input and stores and retrieves it from a database.
*   Write a program that will parse a CSV file and turn it into database entries.
*   Build a simple key/value store.
*   Write an interface for the key/value store that will check the key/value for the key, then if it doesn't exist there, retrieve from database and populate key/value (aka a cache).
*   Build a program that will fetch a web page and tell you the title.
*   Build a program that listens on a socket and echos back any input it receives.
*   Build a program that will give you the word count for every word in a text file.
*   Build a program that can run as a daemon.
*   Build a program that will serve a \"Hello World\" web response from a local url.
*   Write a simple chat server/client
*   Write a web server that will serve the contents of a local directory.

### Summary

Having had no formal education in Computer Science, I have read more than my fair share of \"Teach Yourself 3D Graphics in 24 hours\" books. Many, many of these books are a waste of time, because they don't focus on the sort of operations that you need to do all the time. Things like string manipulation, data math, these are almost ubiquitous in every application you will write and you will do yourself a favor by becoming relatively proficent at them. Some books try to offer resources on the Internet that are available, but its just the nature of publishing that many of these will be gone or out of date, so you need to do that homework up front. I break these up because it can kill your flow Googling around for some reference when you could
