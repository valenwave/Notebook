# The rules of JavaScript Automatic Semicolon Insertion
The JavaScript parser will automatically add a semicolon when, during the parsing of the source code, it finds these particular situations:

when the next line starts with code that breaks the current one (code can spawn on multiple lines)
when the next line starts with a }, closing the current block
when the end of the source code file is reached
when there is a return statement on its own line
when there is a break statement on its own line
when there is a throw statement on its own line
when there is a continue statement on its own line
