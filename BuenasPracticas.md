# Coding Standars 
* Python: PEP 8 => https://www.python.org/dev/peps/pep-0008/


### Consistent Indentation

**Tabs or Spaces?**

Spaces are the preferred indentation method.
Use 4 spaces for each level.
Tabs should be used solely to remain consistent with code that is already indented with tabs.

```
# Aligned with opening delimiter.
foo = long_function_name(var_one, var_two,
                         var_three, var_four)

# Add 4 spaces (an extra level of indentation) to distinguish arguments from the rest.
def long_function_name(
        var_one, var_two, var_three,
        var_four):
    print(var_one)

# Hanging indents should add a level.
foo = long_function_name(
    var_one, var_two,
    var_three, var_four)


# The closing brace/bracket/parenthesis on multiline constructs  may be lined up under the first character of the line that starts the multiline construct, as in:

my_list = [
    1, 2, 3,
    4, 5, 6,
]
result = some_function_that_takes_arguments(
    'a', 'b', 'c',
    'd', 'e', 'f',
)

# Line Break Before Binary Operator

income = (gross_wages
          + taxable_interest
          + (dividends - qualified_dividends)
          - ira_deduction
          - student_loan_interest)

```

### Limit Line Length

**Maximum Line Length**

Limit all lines to a maximum of 79 characters.

```
// bad
$query = "SELECT id, username, first_name, last_name, status FROM users LEFT JOIN user_posts USING(users.id, user_posts.user_id) WHERE post_id = '123'";
 
// good
$query = "SELECT id, username, first_name, last_name, status
    FROM users
    LEFT JOIN user_posts USING(users.id, user_posts.user_id)
    WHERE post_id = '123'";
```

### Consistent Naming Scheme

There are a lot of different naming styles. The following naming styles are commonly distinguished:

* b (single lowercase letter)
* B (single uppercase letter)
* lowercase
* lower_case_with_underscores
* UPPERCASE
* UPPER_CASE_WITH_UNDERSCORES
* CapitalizedWords (or CapWords, or ***CamelCase*** -- so named because of the bumpy look of its letters [4]). This is also sometimes known as StudlyCaps.

Note: When using acronyms in CapWords, capitalize all the letters of the acronym. Thus HTTPServerError is better than HttpServerError.

* mixedCase (First letter of each word is capitalized, except the first word.) 

#### Naming Conventions:
- **Package and Module Names** should have short, ***all-lowercase names***. Underscores can be used in the module name if it improves readability. The use of underscores is discouraged.


- **Class Names** should normally use the ***CapWords / CamelCase*** convention.

- **Function Names, Variable Names, Method Names and Instance Variables** should be ***lower_case_with_underscores***, as necessary to improve readability. ***mixedCase*** is allowed only in contexts where that's already the prevailing style, to retain backwards compatibility.

- **Constants** are usually defined on a module level and written in ***UPPER_CASE_WITH_UNDERSCORES***. Examples include MAX_OVERFLOW and TOTAL.

**Names to Avoid** 

Never use the characters 'l' (lowercase letter el), 'O' (uppercase letter oh), or 'I' (uppercase letter eye) as single character variable names. In some fonts, these characters are indistinguishable from the numerals one and zero. When tempted to use 'l', use 'L' instead.


### Imports
Imports should usually be on separate lines:

```
import os
import sys

from subprocess import Popen, PIPE
```

Imports are always put at the top of the file, just after any module comments and docstrings, and before module globals and constants.

Imports should be grouped in the following order:

1. Standard library imports.
2. Related third party imports.
3. Local application/library specific imports.

You should put a blank line between each group of imports.


### Comments

Comments should be **complete sentences**. The first word should be capitalized, unless it is an identifier that begins with a lower case letter (never alter the case of identifiers!).

**Block Comments**

Block comments generally consist of one or more paragraphs built out of complete sentences, with each sentence ending in a period.

Paragraphs inside a block comment are separated by a line containing a single #.

**Inline Comments**

An inline comment is a comment on the same line as a statement. Inline comments should be separated by at least two spaces from the statement. They should start with a # and a single space.

Inline comments are unnecessary and in fact distracting if they state the obvious.

**Documentation Strings**

*For conventions for writing good documentation strings (a.k.a. "docstrings") see PEP 257.*

Write docstrings for all public modules, functions, classes, and methods. Docstrings are not necessary for non-public methods, but you should have a comment that describes what the method does. This comment should appear after the def line.

```
    """Return a foobang

    Optional plotz says to frobnicate the bizbaz first.
    """
```
Note that most importantly, the """ that ends a multiline docstring should be on a line by itself. For one liner docstrings, please keep the closing """ on the same line.

