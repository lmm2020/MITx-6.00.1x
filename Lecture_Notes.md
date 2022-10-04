# Week 1

## 1. Introduction to Python

Declarative knowledge refers to statements of fact. 
Imperative knowlefe refers to "how to" methods.

Computers often work with imperative knowledge to help us solved problems.

Algorithm: conceptual idea, set of instructions that achieves a result. 
  ALL algorithms have:
    1. a sequence of simple steps
    2. a flow of control process that specifies when each step is executed.
    3. a means of determining when to stop. 


Program: concrete instantiation of an algoritm
  Fixed program computer: calculator, Turing's bombe
    
  Stored program computer: is a computer designed to load and calculate different programs, like a laptop that does many things.
  
  Program counter: points the computer to the next instruction to execute in the program. 

Computational mode of thinking means that everything can be viewed as a math problem involving formulas and numbers.

Computers can: perform calculations & remember results. 
  Made of:
    1. Memory, to store data and instructions for computing
    2. Arithmetic Logic Unit (ALU), computes simple calculations with data stored in the computer's memory.
    3. Control Unit, keep track of what operation the ALU should perform at a specific moment in time (using a program counter)

Syntax: determines if a string is legal
Syntactic errors: example: "hi"5
Static semantic: determines whether a string has meaning
Static semantic errors: example: "The sky is heavy" passes on syntax, but is invalid by static semantics - no one can weigh the sky, so this doesn't mean anything.
Semantics: assigns meaning to a legal sentence.  // "The sky is blue" both pass on syntax and static semantics (as above) and also on semantics - this is a meaningful sentence.

Objects can come as:
  Scalar objects: cannot be subdivided into smaller parts
      example: int, floats, bool, NoneType (special, value=None)

  Non-scalar objects: have an internal structure that can be accessed
      examples: string 

Casting: changing a variable's type. 

+= increments and reassigns to variable 

Priority of Order Boolean Operations
1. Parenthesis
2. not
3. and
4. or

Logic Operators on Booleans
  not a      - will return the opposite of the true/false value that a is
  a and b        - will return True only if both a and b are true
  a or b         - will return True if either a or b are true

## 2. Core Elements of Programs

variable binding with =  (this refers to assigning a value to a variable, ex. y = 5) 


Strings: enclosed in quotations 
concatenate: use + to put together strings
  you can also use arithmetic to strings ex. 3*'eric' would output ericericeric

len() will return the number of characters in a string 
 
slice: 
  [start point: end point (not incl)] 
  [:end point] returns everything from beg up to end point (not incl end point) 
  [:] returns copy of the string
  [start point:] returns beg point to end

advanced string slicing:
  [start:end:increment]
  

input() 
  this will evaluate whatever is input and return a string. 
  if you want it to return and int you must cast it as int.

IDE: Integrated development environment (text editor)

Conditionals: A branching program can be run down many different ways depending on the outcome of a test.

  Use conditional statements (if, else, elif) to perform a test

  if 2 > 3:                              - a test that will either output true or false
      print(“2 is greater than 3!”)      - what to do if the test outputs true

  else:                                  
      print(“2 is not greater than 3.”)  - what to do if the test outputs false

  elif gives the conditional another test to check if the first one outputs false. There can be multiple elif operators in a conditional. 


Loops are programs that repeat themselves until they satisfy some condition.
  For loops have a known number of iterations
  
  While loops have an unknown number of iterations

  both while and for loops can end early with a BREAK statement 
      break statement: special key word that stops the execution of that loop/code
    - immediately exits whatever loop it is in
    - skips remaining expressions in code block
    - exits only innermost loop

loop  characteristics
  need a loop variable
  **initialized outside loop** important to do this!!
  changes within loop 
  test for termination depends on variable

useful to think about a decrementing function
  when loop is entered, value is non-negative
  when value is <= 0, loop terminates and,
  value is decreased every time through loop

range(start, stop, step)

    -The start is the start value for the range() function -(included in output).
    -The stop is the end value for the range() function (not included in output).
    -The step is the number of values to skip between each outputted value. 


# Week 2
## 3. Simple Algorithms
guess and check method: this is an algorthim caled exhaustive enumeration
  you guess a value
  check if solution is correct
  keep guessing until solution found, or guessed through all values

Approximate Solutions 
  we guess and increment by a small value(epsilon) to arrive at a good enough solution 
  -decreasing epsilon -> slower program
  -increasing epsilon -> less accurate answer


Bisection search is the process used to guess a value for a solution, 
    check whether that value is too high or too low to be correct, 
    eliminate all other values that may be too high or too low as well, 
    and keep guessing from the remaining values until a solution is found or all possible values have been guessed

Floats and Fractions
  floats approximate real numbers
  internally, computer represents numbers in binary 

Converting decimal integer to binary in Python!:
num = x

  if num < 0:
    isNeg = True
    num = abs(num)
  else: 
    isNeg = False
  result = ' '
  if num == 0:
    result = '0'
  while num > 0:
    result = str(num%2) + result
    num = num // 2
  if isNeg:
    result = '-' + result 

Newton-Raphson: a general approximation algorithm that finds roots of any polynomial in on variable.  (the root of an equation for example.)

## 4. Functions
   Decomposition and Abstraction
    abstraction: the idea that you can use a block of code and not need to know what's inside it. (ex: once a function is built, you dont need to know *how* it works, but can trust it to do what it's built for.)
    decomposition: breaking up a larger problem into smaller pieces. These pieces are meant to be reuseable. 

  Functions and Scope
    Functions: blocks of code you can reuse over and over through your code. They are like compartments in your software that store code for later use. 
    Name: functions have a name 
    Parameters: arguments that a function can take, it can have zero OR you can set as many parameters as you need, and they can be any data type, even functions!    
    (this is called Higher Order programming)
    Docstring: every function should have a docstring; documentation that tells you what it does. 
    Body: sequence of commands that we want to have happen when we use the funciton. 
  
  Variable Scopes
    global scope refers to the entire piece of code 
    a separate scope exists when referring to variables inside a function 
    
    no return statement in a function results in None value. Always provide function a return statement.
     return vs print
      return only has meaning inside a function, can only occur once inside function 
      print can be used outside functions, and execute many print statements 
  
   Keyword Arguments
    arguments are values given to functions to work with. aka parameters. 
    the function is invoked by typing the function name and includes the parameters required. 

   Specifications
    specification is like a contract between the implementer of the function and the client who will use it, via docstring. 
    Docstrings are good programming practice that states what the function will do, and any conditions. 
 Functions and Scope
    global scope is different from smaller scopes
    functions can be used as arguments of a function
    
  Iteration vs Recursion
  Inductive Reasoning
  Towers of Hanoi
  Fibonacci
  Recursion on non-numerics
  Files 
