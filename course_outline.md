# Introduction to Python Programming for Earth Scientists

## High-level concepts

There are 3 areas: programming and computing concepts, skills, and scientific concepts that motivate the development of the other two.

### Computing concepts

1. Computers and programming in general
  - How data is represented
  - How programs work
  - Version control
2. Tools
  - Unix shell navigation
  - Jupyter notebooks
  - Organizing files and folders for projects
3. Python language
  - Operators, variables, and basic data types
  - More complex data types
  - Modules and libraries
  - Functions
  - Flow control
  - Classes and objects
  - Input and output
  - Exception handling
4. Scientific Python
  - Numpy
  - Matplotlib
  - Pandas
  - Xarray
  - Scipy
5. Working with data
  - Common file formats

### Computing skills

1. Write procedural programs to perform calculations
2. Read data from a file
3. Create plots of data
4. Analyze data by performing calculations on arrays

### Scientific concepts

1. Planetary surface temperature is controlled by solar radiation, albedo, and greenhouse gases


## Modules and learning goals

1. Computers and computing environments
2. Python basics
3. Functions
4. Flow control
5. Introduction to Python tools for scientific computing


...(THE BELOW TO BE DEVELOPED FURTHER)

8. Classes and objects
9. Arrays and NumPy
10. Pandas and Xarray
11. Applications

### Computing Environments

#### Computing concept goals and level
- Identify that computers use binary to represent information 1
- Transform between decimal and binary numbers 1
- Describe how computers represent integers, floating point numbers, and alphanumeric characters 1
- Describe the difference between an interpreted and compiled programming language 1
(- Explain what a version control system does and why it is useful 3)

#### Computing skill goals and level
- Be able to log on to the JupyterHub and create, edit, save, and upload/download files. 1
- Create formatted text in notebook cells with markdown. 1
- Create basic equations with LaTeX in notebook cells. 1
- Navigate a unix file system using shell commands. 2
- Use the ! operator to execute shell commands from a notebook
- Stop and start notebook kernels
(- Create nd manage a git repo 3)
(- Manage own project w gh 3)
(- Collaborate w gh 4)
(- Be able to install and operate a scientific python distribution on your own computer. 4)

#### Scientific concept goals and level
- Define solar irradiance and albedo 1
- Identify the Stefan-Boltzmann law 1
- Use the Stefan-Boltzmann law to calculate the effective radiating temperature of earth or any other planet given S0 and albedo 2

#### Exercise and assignment notes
- First practice in notebook math and markdown writing formulas for surface area of circle and sphere
- Then have them take notes in the notebook using markdown and latex as I go over incoming solar radiation and Stefan-Boltzmann law
- Have them download a file of irradiance data, and upload it to the hub
- Have them make a folder and sub-folder for their data file, and inspect its contents with cat and more, and write down a "typical" value from the file in their notebooks
- For binary, have them calculate how many binary digits are needed to represent the (integer) values 1370 (Solar contant), 10000, 100000, etc. (turns out it's floor(log2(N))) - maybe have them import math and use log2 and floor.

### Python basics

#### Computing concept and skill goals

- Operators
  - Perform calculations using Python arithmetic operators
  - Describe operator order-of-precedence
- Variables (basic types)
  - Use the assignment operator to create or update a variable
  - Define dynamicically typed programming language
  - Identify the basic data types in Python
  - Determine the type of a variable
  - Convert between basic data types
  - Execute Python commands in an interpreter
  - Use %whos to list the variables stored in the memory of the python kernel
  - Collect user input using the input() command
- Variables (more complex types)
  - Describe the str, list, dict, tuple, and set data types
  - Define and extract elements from strs, lists, and dicts
  - Recognize tuples and sets
  - Create compound data types (e.g., a dict that contains lists as values)
  - Define immutable versus mutable data types

#### Scientific concept goals and level
- Define greenhouse gas and greenhouse effect 1
- Explain the faint young sun concept 1
- Combine the Stefan-Boltzmann law with incoming solar energy to solve for earth's equilibrium radiating temperature 2
- Explain how and why irradiance is different for different planets

### Functions

#### Computing concept and skill goals

- Working with functions
  - Call functions using arguments by position or keyword
  - Handle function returns, including multiple returns
  - Import modules using the `import <name>`, `from <module> import`, and `import <name> as <shorthand>` syntax patterns
  - Call functions imported from modules using these different methods
  - Use the question mark syntax to get help on a function
- Writing your own functions
  - Describe why functions are useful
  - Define "parameter" and "argument"
  - Write functions that use required and optional arguments
  - Write functions that return one or more values
  - Explain the difference between argument passing by copy or by reference, and what kinds of variables they apply to
- Optional
  - Understand (+ use) what the **kwargs pattern means
  - Understand (+ use) what the *args pattern means
  - Use recursion
  - Write a docstring to provide help for your function

#### Science concept goals

TBA

### Flow control

- Conditionals
  - Use `if-elif-else` to branch code execution
  - Use `and`, `or`, `not`
  - Optional
    - Use the `^` (xor) operator and xor() function
    - Use bitwise operators `&, |, ^, ~`
    - Use bitwise shift operators `<<, >>`
- Loops
  - Explain why loops are useful in general
  - `for` loops
    - Explain what a `collection` means in the context of looping through items in a collection
    - Describe and use the `range` function (as you would a list)
    - Use a `for` loop:
      - to iterate through items in a list
      - with a counter variable and the `range` function
      - do the above using different start, end, and increment values
      - do it with decrementing (negative increment)
  - `while` loops
    - Identify circumstances where a `for` or `while` loop is preferable
    - Write a `while` loop
    - The above with an "escape variable" (e.g., `done == True`)
  - Use `break` to get out of a loop (and explain why that's not usually best practice)


#### Science concept goals

TBA

### Tools for scientific computing

#### Computing concepts and skills

- Arrays and NumPy
  - Create 1D arrays using `array, zeros, ones`, and use them in arithmetic expressions
  - Describe the differences between arrays and lists
  - Use `arange` and `linspace` to create arrays that are sequences of values
  - Access elements or subsets of arrays using slicing
  - Use the size and shape methods to interrogate arrays
  - Use the `mean, amax, amin, median, sum` functions with arrays
  - Use the `maximum` and `minimum` functions to find the min/max on an element-by-element basis
  - Explain the difference between creating a copy of a reference to an array and creating a new copy of an array using copy()
  - Explain what array dereferencing is, and how to avoid it
  - Create 2D or 3D arrays
  - Create arrays of type other than float
  - Use boolean array expressions to access selected array elements
  - Optional
    - Use `argmin, argmax, where` to find array indices where are condition is true
    - Sort an array
    - Flip an array
    - Generate and apply random numbers using the np.random module's `rand` and `randn` functions
- Matplotlib
  - import the pyplot sub-package
  - x-y plotting basics
    - use the `plot` function with lists or arrays to create basic x-y plots
    - recognize that the `scatter` function is similar but with some differences (e.g., defaults to marker rather than line)
    - vary the line/marker style and color
    - add axis labels to a plot
    - add a title to a plot
    - plot multiple quantities on the same plot
    - use a legend
    - set the axis extents with `xlim, ylim`
    - add gridlines
    - change line or marker opacity, color, style, and width
  - anatomy of matlplotlib plots and axes
    - explain what a `plot` and an `axis` are
    - use `gcf` to get the current figure and `gca` to get the current axis
    - use `figure()` to create a new figure and get a handle to it
    - access two examples of functions or properties from `ax` (e.g., invert_yaxis)
    - optional
      - use `subplots()` to create one or more axes in a figure and get handles to the figure and axis
      - create a plot with multiple axes
  - optional
    - use `bar` to make bar charts with standard deviation
    - name 2 or 3 examples of Python plotting packages
    - use `fill` to fill in areas
    - use `text` to add text
- file I/O
  - basics
    - open, write to, and close a text file using `open, write, close`
    - do the above using the `with` syntax
    - open, read from, and close a text file using `with, open, read`
    - read lines individually `readlines`
    - split lines by column using string .split() (potential exercise: file with "Mercury 1\nVenus 2..." etc., read the lines then loop over lines to create a dict with name as key and number as int value)
    - as above, for csv files
  - via numpy
    - define what a comma-separated value or csv file is
    - read a file with delimited numbers (only) using `loadtxt`
    - read a file with missing values and/or text content using `genfromtxt`
    - skip header rows when using either of the above functions
- pandas
  - Define tabular data
  - Create a DataFrame directly from sample data
  - Read a csv into a DataFrame
  - Read other tabular data using read_table
  - Display a DataFrame as a table
  - Add columns to a DataFrame
  - Plot data from two columns from a DataFrame
  - Write modified DataFrame contents to a text file





## Schedule and Lesson Plans

### Module 1: Getting started with scientific computing

#### Introduction

- Introduction and mini-lecture on computing in geoscience (10 min)
- Intro to course and syllabus (10)
- Intro to notebooks (5)
- Ex: log on to J-hub; sort out any issues (5)
- Overview of the Lab environment: file browser, tools, tabs window (5)
- Overview of J notebooks (5)
- Open daily notebook and do exercise of name, date, note to self about the Python print() function, and hello world (5)
  - Directions: make a new notebook, give it a name that includes today's date.
  - Make a text cell that has a 1st-level heading "Getting started", name, and date
  - Make a new text cell, give it a 2nd-level heading "The Python print() function", then write a note to your future self about what the function does.
  - Make a new code cell with a print("Hello, world!") and run it
- Live guided exercise on LaTeX math, with inline ($g=9.8$ meters per second squared) ($\pi$), own line ($$A_c = \pi r^2$$, $$A_s = 4 \pi r^2$$) (10)
  - Make a new text cell with the 2nd-level header "LaTeX math"
  - Write some expressions or equations, including at least one subscript, one superscript, and Greek symbol, one fraction, and one square root. Include at least one example of an inline equation, and one example of an equation on a line by itself.
- Mini-lecture on geologic time by powers of ten (10)
- Wrap up and recap (5)

#### Operators

- Motivating example and mini-lec on planetary temperature; take notes in a markdown cell(s) with latex math in today's notebook. Part 1: energy balance in words and formula for power input rate. (10)
  - Make a title, and a heading "power from the sun"
  - Use markdown text and latex math to take notes
- Intro to operators: Enter numbers for 3.1416 * 6370 ** 2; get someone to identify the units; explain what operators are. Show some basics: 1 + 1, 3 - 1, 2 * 3, 3 / 2, 3 ** 2. What if more than one?  (10)
  - Try the calc in a code cell and see what you get
  - Try it with parens around (6370 * 2)
  - Try to put parens that give you the WRONG answer
  - Guess what 2 + 3 * 4 is, then try it
  - Try (2 + 3) * 4
  - Guess what 4 / 2 * 3 is, then try it
  - Try 3 * 4 / 2
  - Try to get the right answer to (1 + 5) / (2 * 3) (but write it in standard math without parens)
  - Conclude talking about operator precedence.
- Part 2: blackbody radiation and S-B law (10)
- Solar irradiance: exercise in downloading data, uploading it to hub (5)
- Guided exercise on unix shell commands: introduce pwd, ls, cd , .. and ., mkdir, mv, cp, cat, more. (5)
- Then have them create a directory for the solar irradiance data, move the file into it, and use cat or more to look at the values. What's a typical value? (10)
  - Write a notebook cell that lists the unix commands we reviewed and briefly says what they do
  - Do a !ls in a code cell as an example of using ! to run shell commands from a notebook
- How computers represent data; RAM and storage; bits and bytes; binary numbers with example of earth radius in km; have them to pCO2 in ppm, and density of quartz. (10)
  - In a code cell, calculate and print the 0-11 powers of 2
  - In a markdown cell, write the binary for pCO2 ppm and density of quartz; test by adding up the 1's
- Guided live ex: how many binary digits needed for 100 ky, 10 my, 1 Gy? (5)
- Guided exercise: python import statement, and use of math log2 and floor functions (5)
  - Try math.log2(2650)
  - Try math.floor(2650)
- Wrap up and assignment (5)

#### Materials

- Slides and/or notes and/or Jbook
  - Intro to course
  - Geologic time by powers of 10
  - Planetary temperature & bb rad
  - Binary representation
- In-class workbooks
  - Day 1 - they create their own
  - Day 2


### Module 2: Python Basics

#### Variables, part 1

- Science opener: earth radiating temperature. Greenhouse effect. Radiating temperature on Mars, Venus, Mercury. (10)
- Variables. Notice that we're having to re-type numbers. Useful if you could store values for later reuse. That's what variables are. Demo: define sigma in a variable then reuse. (5)
- Assignment operator as an instruction to the computer. (5)
  - nbex: define vars for each factor in the temperature equation and use them to calculate the temperature and print it. (5)
- How does Python know whether float or int or something else? Automatic typing. type() function. (5)
- Integer, string.
  - nbex: pick one of the planets we looked at. Define a string var for the planet's name, an integer for the number (Mercury=1), and a float for the solar irradiance. Use type() to verify that each var is of the type you intended. (5)
  - Try casting S0 to an int. What happens? Cast to str, what happens? Try planet number to float. What happens?  (5)
  - Try 2 = (1 + 1). Then 2 == (1 + 1). Then result = 2 == (1 + 1). type(result) (5)
- Comparison operations and bool variables. (5)
  - Try: result == True, result is True, result is False, result is not False. Which expression evaluates to False? (5)
- Redefining. Try reusing a variable, eg sigma, so sigma = "I forgot". type(sigma). Previous contents are discarded and variable is redefined (in general, avoid doing this!). (5)
- Discovering variables in your notebook with %whos.
  - nbex: run %whos in a code cell; make a note to yourself that this is a notebook command not a Python function. (5)


#### Variables, part 2

- String indexing.
  - nbex: epoch = "Anthropocene". len(epoch). epoch[0]. Use brackets to print the "ro" in "Anthropocene" (5)
  - try epoch[12]. Lesson: 0-based indexing. (5)
  - ranges with colon. Ex: epoch[2:7]. epoch[:2]. epoch[7:]. (5)
  - try period = "Cretaceous". Use slicing to print out the phrase 'Creta' means 'chalk'. (5)
- REST TO BE ADDED... lists, dicts, tuples, sets - consider learning goals of being able to work with list and dict, and being able to describe and recognize a tuple or set









  


