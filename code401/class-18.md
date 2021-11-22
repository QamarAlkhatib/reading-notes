# Automation

## Regular Expressions in Python

In Python, regular expressions are supported by the re module.

```python
import re
```

### Basic Patterns: Ordinary Characters

You can easily tackle many basic patterns in Python using ordinary characters. Ordinary characters are the simplest regular expressions.

Examples are 'A', 'a', 'X', '5'.

Ordinary characters can be used to perform simple exact matches:

```python
pattern = r"Cookie"
sequence = "Cookie"
if re.match(pattern, sequence):
    print("Match!")
else: print("Not a match!")

# output: Match!
```
The match() function returns a match object if the text matches the pattern. Otherwise, it returns None

### Wild Card Characters: Special Characters

When employed in a regular expression, special characters are characters that do not match themselves as viewed but have a specific meaning. They can be regarded of as reserved metacharacters that denote something other than what they appear to be for a simple understanding.

- ```search()``` : search function, you scan through the given string/sequence, looking for the first location where the regular expression produces a match. 

- ```group()```: group function returns the string matched by the re.

- Examples:

```python
re.search(r'Co.k.e', 'Cookie').group()
# output 'Cookie'
```

-------------- --

## shutil — High-level File Operations

The shutil module includes high-level file operations such as copying and archiving.

- Copying Files

```python
import glob
import shutil

print('BEFORE:', glob.glob('shutil_copyfile.*'))

shutil.copyfile('shutil_copyfile.py', 'shutil_copyfile.py.copy')

print('AFTER:', glob.glob('shutil_copyfile.*'))

# output
# BEFORE: ['shutil_copyfile.py']
# AFTER: ['shutil_copyfile.py', 'shutil_copyfile.py.copy']

```

The implementation of copyfile() uses the lower-level function copyfileobj(). While the arguments to copyfile() are filenames, the arguments to copyfileobj() are open file handles. The optional third argument is a buffer length to use for reading in blocks.

```python

shutil_copyfileobj.py

import io
import os
import shutil
import sys


class VerboseStringIO(io.StringIO):

    def read(self, n=-1):
        next = io.StringIO.read(self, n)
        print('read({}) got {} bytes'.format(n, len(next)))
        return next


lorem_ipsum = '''Lorem ipsum dolor sit amet, consectetuer
adipiscing elit.  Vestibulum aliquam mollis dolor. Donec
vulputate nunc ut diam. Ut rutrum mi vel sem. Vestibulum
ante ipsum.'''

print('Default:')
input = VerboseStringIO(lorem_ipsum)
output = io.StringIO()
shutil.copyfileobj(input, output)

print()

print('All at once:')
input = VerboseStringIO(lorem_ipsum)
output = io.StringIO()
shutil.copyfileobj(input, output, -1)

print()

print('Blocks of 256:')
input = VerboseStringIO(lorem_ipsum)
output = io.StringIO()
shutil.copyfileobj(input, output, 256)

# output
# Default:
# read(16384) got 166 bytes
# read(16384) got 0 bytes

# All at once:
# read(-1) got 166 bytes
# read(-1) got 0 bytes

# Blocks of 256:
# read(256) got 166 bytes
# read(256) got 0 bytes

```