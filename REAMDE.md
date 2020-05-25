# DM 103411: Simple Recursive Decent Parser #
### PROJECT MEMBERS ###
StdID | Name
------------ | -------------
**60486** | **M. Areeb Aslam**
61521 | Faariha Khan
## Project Description ##
The goal of this project is to implement Simple Recursive Descent Parser and combine it with a Lexical Analyzer in C#. We are creating a GUI to generate a recursive decent parser and lexical analyzer also.

## Sample Language Used ##
We are using C# to build this project
```C#
List<List<int>> rules = new List<List<int>>();
        private void loadTransitionTable(string path)
        {
            string text = System.IO.File.ReadAllText(path);
            if (text.Length < 2)
            {
                throw new Exception();
            }
            foreach (var item in text.Split('\n'))
            {
                var temp = new List<int>();
                foreach (var itm in item.Trim().Split(' '))
                {
                    temp.Add(Convert.ToInt32(itm));
                }
                rules.Add(temp);
            }
        }
```
### Lexical Specification ###
Lexical analyzer is a program to recognize tokens from an input code. Each token is a meaningful character string, such as a number, an operator, or an identifier.
Following are the rules of lexical analyzer
- Case insensitive
- All English letters (upper and lower), digits, and extra characters as seen below, plus whitespace
- Identifiers
- Keywords (reserved), include: start finish then if repeat var int float do read print void return dummy program
- Relational operators, include: == < > =!= => =<
- Other operators, include: = : + - * / %
- Delimiters, include: . ( ) , { } ; [ ]
- Numbers


### Grammar ###
This specification presents the C# programming language using grammars. The lexical grammar defines how Unicode characters are merged to form line terminators, white space, comments, tokens, and pre-processing directives to form C# program.

## Problems Faced ##
There are several problems which we have faced during creating a compiler in C#.
### Problem 1: Creating a Lexical Analyzer ###
A simpler design is the most important factor. The separation of lexical analysis from syntax analysis often allows us to simplify one or the other of these phases.

### Problem 2: Generating a Parser in C# ###
We do many researches to generate a Recursive Decent Parser but we just find it in a C programming language. So we take a C code of Parser and convert it in C# which is a difficult task for us. Because we don't have much knowledge about C programming language.

## References ##
- [Lexical Analyzer1](https://dzone.com/articles/writing-compiler-c-lexical)
- [Lexical Analyzer2](https://github.com/yazdipour/csharp-lexical-analyzer)
- [Parser1](https://dzone.com/articles/recursive-descent-parser-c)
- [Parser2](https://www.geeksforgeeks.org/recursive-descent-parser/)
- https://www.researchgate.net/publication/220613313_Object-oriented_recursive_descent_parsing_in_C
- https://stackoverflow.com/questions/11425202/is-it-possible-to-call-a-c-function-from-c-net
- https://stackoverflow.com/questions/21750450/undefined-refrence-to-clrscr
- https://www.quora.com/Which-header-file-is-needed-to-use-clrscr-function-in-C