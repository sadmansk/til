Finding files
=============

Anyone who has worked with `java` knows the pain of having to go through several
directories in order to find a file. If you are using an IDE like Eclipse, it'd
become a lot easier, but there are major problems when using a regular text editor
like vim. The fact that we can just specify a file name which vim finds and opens
for editing is extremely useful in such cases.

### Opening a file from the command line
This is probably the least convenient one. We have to rely on using the bash `find`
utility since vim does not seem to explicitly have a command that would do it for
us:
```
vim $(find -name FILE_NAME)
```

### Opening a file from within vim
In the current window:
```
:find FILE_NAME
```
In a new tab:
```
:tabfind FILE_NAME
```
The :tabfind command uses Vim's 'path' option to determine which directories should
be searched when opening the specified file. For example, the following tells Vim
to look in the directory containing the current file (.), then the current directory
(empty text between two commas), then each directory under the current directory
('\*\*'). 
```
:set path=.,,**
```
