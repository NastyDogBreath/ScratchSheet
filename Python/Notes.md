# Python Notes

## PEP
Stands for Python Enhancement Proposal.  A design document with information to the community for a new feature, process or environment.

This is not about writing awesome code, but by using a set style for clean and attractive code.  PEP 8 is the style guide for Python Code.

## Coding Style Guidelines

Tabs and indentations should be 4 spaces.  Spaces are the prefered method.  Most coding editors will do this automatically.

Two blank lines should seperate blocks of code.

Align with opening delimter when working with the first parameter when breaking lines.

Maximum line length should be 79 characters.

Imports should be in this order
1. Standard Library
2. Third-party Libraries
3. Local application / library

## Class Initialization

`def __init__(self) -> none;`

### Naming

Modules - short, lowercase names

Classes - CapitalizedNaming without underscores

Functions - lowercase_with_underscores

Constants - ALL_CAPS

Private Variables - start with an _underscore

Docstrings for all public modules, functions, calsses and methods.

### pyLint

Linting tool for Python

Others:  bycodestyle, black (fixes code for you)

Can be ran with command line with warnings and a score.

To generate a lint file, use `pylint --generate-rcfile > pylintrc`

`pylintrc` is the default filename for the linting rules.

## PIP

Python Package Libraries

## Documenting your Python Code

PEP - Semantics and conventions for docstrings.

### Docstrings and standards

String as first statement of a module, function, class or method

Becomes the `__doc__` attribute.

Docstrings should use `"""three double quotes"""` Make sure that you use complete sentences.  The `"""` can span multiple lines.

### Sphinx - generates html from source documentation

`pip install sphinx`

Create a new directory for your documentation, eg `docs`.  Go into new directory.  Type `sphinx-quickstart`.  Most of the defaults are fine.  Add the project name, Author and default language.

Python documentation generator.  De-facto standards.

Can export to HTML, PDF and other filetypes.

## Static typing in Python
Type hints, just a general introduction. 

Static Typing - Declares specific variable type in code (Java, C#, ....)

Dynamic Typing - Use a generic type.  (Javascript, Python)

To help strongly type functions, we can do the following which returns an int

`def my_function(par1: int, par2: int, par3: string = "") -> int:`

`age: int = 0`

Using static typing will introduce errors without compilation.

## Abstract Classes

Use `@abstractmethod` above methods to prevent them from being used, and must be inherited.


