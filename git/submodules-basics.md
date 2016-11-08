Submodules basics
=================

`git` submodules are especially useful when we require the use of code from
different repositories, examples include third-party libraries and frameworks.

> Submodules allow you to keep a Git repository as a subdirectory of another
Git repository. This lets you clone another repository into your project and
keep your commits separate. - [git-scm](https://git-scm.com/book/en/v2/Git-Tools-Submodules)

### Add submodules to an existing project
```
git submodule add GIT_REPO_URL
```
By default, submodules will add the subproject into a directory named the same
as the repository.

### The `.gitmodules` file
The above command automatically adds the file to the root directory of the
original repository. The file lists all the submodules added to the project:

```
[submodule "SUBMODULE_REPO_NAME"]
    path = PATH_TO_SUBMODULE_FOLDER
    url = SUBMODULE_REPO_URL
...
```
This file can be manually created and edited.

### Working with projects with submodules
Two ways to do it, first is to clone the original repo and running a couple of
commands to download the submodules:
```
git clone ORIGINAL_GIT_REPO_URL
git submodule init
git submodule update
```
The second way is by passing the `recursive` flag to the `git clone` command:
```
git clone --recursive ORIGINAL_GIT_REPO_URL
```
