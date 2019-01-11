## Lexical Structure
* Notes from Python in a Nutshell, 3rd Edition.
* lowest-level syntax of the language

#### lines and indentation
* a python prog is a sequence of **logical lines** each made up of one or more **physi‐ cal lines**
* **comment** # that is not inside a string literal starts a comment
* **no delimiter**. when a stmt is too long for one physical line, join two adjacent physical lines into a logical line by ensuring that the first physical line has no comment and ends with a backslash \
* auto join: adjacent physical lines are joint into one logical line if an open parenthesis ((), bracket ([), or brace ({) has not yet been closed. 
* **blocks** indentation is the only way to denote blocks. *A block is a contiguous sequence of logical lines, all indented by the same amount; a logical line with less indentation ends the block.*
* Standard Python style is to use **four spaces** (never tabs) per indentation level.


#### character sets
v3 source: Unicode character, encoded as UTF-8
* In both v2 and v3, you may choose to tell Python that a certain source file is written in a different encoding
* To let Python know that a source file is written with a nonstandard encoding, start your source file with **a comment** whose form must be, for example:
    * 
    ```
    # coding: iso-8859-1
    ```

#### tokens