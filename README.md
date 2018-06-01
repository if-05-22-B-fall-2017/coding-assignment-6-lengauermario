# if.06.22 Theoretical Informatics

## NoBeard Project

### Objective
The goal of this assignment is to make you familiar with basic concepts of compiler construction. In particular you shall be practising

- Techniques of writing a Scanner
- Basic parser techniques using recursive descent parsing

### Materials
The given skeleton project is using NetBeans as a development environment. The easiest way to accomplish this exercise is to use NetBeans as well.

### Required Tasks

1. Currently NoBeard supports only line comments: Whenever the scanner reads a "#" the rest of the line is considered to be a comment.
You are to implement block comments in the following way. If the scanner reads the sequence ``(*`` a comment starts and the following part is skipped until the scanner reads ``*)``. Take care that block comments can be nested, i.e., that a comment can be within a comment. Example of a nested comment:
``(* Here is a (*nested*) comment and everything is skipped until here *)``
Take the NetBeans project and enhance the given Scanner class.
Test your implementation with some self-written NoBeard programs

2. Browsing through the source code of the NoBeard Compiler will show you that the ``IfParser`` is already implemented. But in case you try to compile a little program having an if statement you will get the following error message: ``Error in line 5: if is not a statement`` (the actual line number, of course, depends on your source code). This is due to the fact that the ``StatementParser`` does not react on the if-keyword.
Analyze the source code of the ``StatementParser`` and change its implementation such that one can compile NoBeard programs with if-statements using the ``nbc``.
Test your implementation with some self-written NoBeard programs. Prefix the name of the test files with your family name and put them into the folder ``SamplePrograms``.

3. The current implementation of the ``NoBeardCompiler`` does not support any method to get user input. Change the ``KeywordTable`` of the NoBeard ``Scanner`` such that it recognizes the ``get`` keyword correctly (Add the ``Symbol.GET`` to the Scanner).
Study the get-statement of the NoBeard Report as given in the attachment. Implement a class ``GetParser`` such that it can syntactically parse get statements as specified in the NoBeard report.
Adapt the implementation of the ``StatementParser`` such that it reacts to the get-keyword properly.
Test your program thoroughly with some self-written NoBeard programs. Prefix the name of the test files with your family name and put them into the folder ``SamplePrograms``. Take care that your programs test all different possibilities (one or two arguments).

### Evaluation
Despite of its functional correctness the assignment will be checked concerning the

- Quality of the test files created
- Quality of your submitted code

Furthermore randomly picked projects will have to be discussed with the instructor.
