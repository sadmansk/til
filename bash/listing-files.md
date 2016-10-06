Listing files
=============

Useful options:
  - `-t` List files in order of last modification date, newest first. Using `-r`
command along with it shows it in reverse order, i.e. oldest first.
  - `-X` Group the files by extensions. Useful for separating header and source
files, source files and directories, etc.
  - `-v` Naturally sort version numbers in filenames. Useful for listing build or
log arfchives.
  - `-S` Sort by filesize.
  - `-R` List files recursively. This one is especially useful when combined with
`-l` and piped through to `less` or an editor. For example, we could pipe it to
a vim process, so we can add explanations of what each file is for and save it to
a file for bookkeeping or documentation or `README`s:

```
ls -XRl | vim -
```
