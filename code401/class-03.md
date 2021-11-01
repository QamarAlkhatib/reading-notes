# FileIO & Exceptions

## Reading and Writing Files in Python (Guide)

reading a file in python is quite simple since there is a built-in methods for this purpose, and the methods are as follows:

- .read(size=-1) : This reads from the file based on the number of size bytes. If no argument is passed or None or -1 is passed, then the entire file is read.

- .readline(size=-1) : This reads at most size number of characters from the line. This continues to the end of the line and then wraps back around. If no argument is passed or None or -1 is passed, then the entire line (or rest of the line) is read.

- .readlines():   This reads the remaining lines from the file object and returns them as a list.

---

Now let’s dive into writing files. As with reading files, file objects have multiple methods that are useful for writing to a file:

- .write(string): This writes the string to the file.

- .writelines(seq):This writes the sequence to the file. No line endings are appended to each sequence item. It’s up to you to add the appropriate line ending(s).

--------------------

## Python Exceptions

An exception is an event that occurs during the execution of a Python program. It can happen even though the program is already running. This type of error occurs whenever syntactically correct Python code results in an error.


here is an example of built-in exceptions in python:

- ```with_traceback:``` This method sets tb as the new traceback for the exception and returns the exception object

- ```BaseException:```  The base class for all built-in exceptions. It is not meant to be directly inherited by user-defined classes (for that, use Exception). If str() is called on an instance of this class, the representation of the argument(s) to the instance are returned, or the empty string when there were no arguments.

