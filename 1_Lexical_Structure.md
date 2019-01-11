## Lexical Structure
* Notes from Python in a Nutshell, 3rd Edition.
* lowest-level syntax of the language

### lines and indentation
* a python prog is a sequence of **logical lines** each made up of one or more **physi‐ cal lines**
* **comment** # that is not inside a string literal starts a comment
* **no delimiter**. when a stmt is too long for one physical line, join two adjacent physical lines into a logical line by ensuring that the first physical line has no comment and ends with a backslash \
* auto join: adjacent physical lines are joint into one logical line if an open parenthesis ((), bracket ([), or brace ({) has not yet been closed. 
* **blocks** indentation is the only way to denote blocks. *A block is a contiguous sequence of logical lines, all indented by the same amount; a logical line with less indentation ends the block.*
* Standard Python style is to use **four spaces** (never tabs) per indentation level.


### character sets
v3 source: Unicode character, encoded as UTF-8
* In both v2 and v3, you may choose to tell Python that a certain source file is written in a different encoding
* To let Python know that a source file is written with a nonstandard encoding, start your source file with **a comment** whose form must be, for example:
    * 
    ```
    # coding: iso-8859-1
    ```
* the above **coding directive comment** (also known as an encoding declaration) is taken as such only if it is at the start of a source file

### tokens
* Each token corresponds to a substring of the logical line. 
* The normal token types are 
    1. identifiers 
    1. keywords 
    1. operators 
    1. delimiters
    1. literals

#### identifiers
* 
    *  starts with a letter (in v2, A to Z or a to z; in v3, other characters that Unicode classifies as letters are also allowed) or an underscore (_)
    * followed by zero or more letters, underscores, and digits (in v2, 0 to 9; in v3, other characters that Unicode classifies as digits or combining marks are also allowed
    * Punctuation characters such as @, $, and ! are **not allowed** in identifiers.
* **Python conventions**:
    * class name: start with cap
    * other ids: start with lower case 
    * 
        ```
        _someName   # this id is meant to be private
        ```
    * 
        ```
        __someName  # this is a strongly private identifier
        ```
    * 
        ```
        __someName__  # this is a language-defined special name
        ```

#### keywords
* v2: 31
* v3: 33
* Keywords contain lowercase letters only
* Reserved for special syntactic uses
* keywords may mark the beginning of a simple stmt or a clause of a compound stmt, or serve as operators

#### operators
* use nonalphanumeric characters and character combinations as operators

#### delimiters
