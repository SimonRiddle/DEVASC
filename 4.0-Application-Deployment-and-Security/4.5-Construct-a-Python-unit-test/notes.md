<!-- cSpell:ignore  pytest,-->

# Construct a Python unit test

## Overview

* Detailed testing on small bits of code
* Typically automated testing, via unit test frameworks
* Uses assertions, saying xyz should equal abc, if it doesn't - you have a problem!

Example:-

```python
a = 2 + 2
assert a == 4
```

The below would require an error:-

```python
assert a == 5
```

## Frameworks

* unittest
    * Included in Python by default
    * Enables test collections as methods extending a default TestCase class
    * Automatically ran against functions/files prefixed with test_ or suffixed _test.py
* PyTest
    * Not included by default *pip install pytest*
    * Can run unittest without any modification
    * Build tests as functions, rather than class methods
    * Usually used by more specialized test suits

