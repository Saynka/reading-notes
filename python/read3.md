# FileIO & Exceptions

## Refrences 

* https://docs.python.org/3/library/functions.html#open

* https://realpython.com/python-exceptions/

* https://realpython.com/read-write-files-python/

* https://realpython.com/courses/reading-and-writing-files-python/

* Reading and Writing Files in Python Quiz

## What is a file?

* At its core, a file is a contiguous set of bytes used to store data. This data is organized in a specific format and can be anything as simple as a text file or as complicated as a program executable. In the end, these byte files are then translated into binary 1 and 0 for easier processing by the computer.

## Three main parts of a file

* Header: metadata about the contents of the file (file name, size, type, and so on)
* Data: contents of the file as written by the creator or editor
* End of file (EOF): special character that indicates the end of the file

## File paths

* Folder Path: the file folder location on the file system where subsequent folders are separated by a forward slash / (Unix) or backslash \ (Windows)

* File Name: the actual name of the file

* Extension: the end of the file path pre-pended with a period (.) used to indicate the file type

## Opening and Closing a File in Python

* When you want to work with a file, the first thing to do is to open it. This is done by invoking the open() built-in function. open() has a single required argument that is the path to the file. open() has a single return, the file object:
* open a file - file = open('dog_breeds.txt')
* close a file - try:
     Further file processing goes here
finally:
    reader.close()

## Exceptions Versus syntax errors

* Syntax errors occur when the parser detects an incorrect statement.

## The AssertionError Exception

* Instead of waiting for a program to crash midway, you can also start by making an assertion in Python. We assert that a certain condition is met. If this condition turns out to be True, then that is excellent! The program can continue. If the condition turns out to be False, you can have the program throw an AssertionError exception.

## key points 

* raise allows you to throw an exception at any time.

* assert enables you to verify if a certain condition is met and throw an exception if it isn’t.

* In the try clause, all statements are executed until an exception is encountered.

* except is used to catch and handle the exception(s) that are encountered in the try clause.

* else lets you code sections that should run only when no exceptions are encountered in the try clause.

* finally enables you to execute sections of code that should always run, with or without any previously encountered exceptions.


