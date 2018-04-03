# Evaluate Arithmetic expressions

Coding solutions tmathevalprogramo arithmetic expression evaluation

Solution Number One:

  Limitations
    - The first code uses the two stack approach of Dijkstra's algorithm. 
    - It assumes the expression is parenthenized and ignores whitespace, if there are any.
    - It assumes only single digits in the expression.
  
  Operation
    - Logic for program explained in Coursera's Princeton Algorithm Part 1, Video titled, Stack and Queue Applications (optional) https://www.coursera.org/learn/algorithms-part1/lecture/2Mbvz/stack-and-queue-applications-optional. Course is  taught in Java but logic/principles are same for C++.
    - A For Loop program that checks:
    - Checks to see if token is digit.  If digit, pushes to number stack.  Because the expression passed into function as string, if token is digit, it must be converted to integer before being pushed into the number stack.  Subtract 48 fom token.  48 is ascii for 0.  Subtracting 48 for char token will yield 0 to 9.
    - If not a digit, check for left parenthesis, is so, continue to next token.
    - Checks for Operator and pushes to sign stack.
    - If left parenthesis, pop operator and top two values from number stack.
    - Perform arithmetic operation and push result back to number stack.
    -After For Loop completes, pop remaining value in number stack and return to main.
 
 
Solution Number Two:

  Limitations
    - It assumes the expression is NOT parenthenized and ignores whitespace, if there are any.
    - It will not solve parenthenized expressions
    - It assumes only single digits in the expression.
    - Does not perform Power To calculations or Square Root, etc, but conditionals can be modified to do that.
  
  Operation
    - Logic performs for loop to perform all multiplications and divisions first.
    - Results of multiplications and divisions push back to stack in correct position, with for loop exiting once that is all         done.
    - Two separate while loops reverses the sign stack and number stack by push it onto a new set of stacks.
    - New stacks reverses the numbers and signs so that it now reads left to right correctly.
    - Additions and subtractions are done left to right to produce the correct answers.
    - Check limitations for Solution One for similar issues.
  
 
Infix to Postfix Solution:
 
  Limitations
    - It assumes only single digits in the expression.
    - Does not perform Power To calculations or Square Root, etc, but conditionals can be modified to do that.
    
  Operation
    - First converts infix to postfix notation
    - Second evaluates postfix notation
    - Commented out "cout" statements through out implementation file are debugging statements to assist me and can be 
    ignored.
    
Matching Parenthesis

  limitations 
    - none, checks for all 3 types of brackets
    
  Operation
    - uses one stack
    - only pushes opening brackets to stack
    - closing brackets checked and discarded
