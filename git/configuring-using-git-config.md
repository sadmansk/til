Configuring using `git config`
==============================

To start off, the command `git config` lets the user set up any configuration
values without having to manually edit either the global or local git config files.
The flag `--global` is used when the global config file is modified, otherwise
the local file is used. The second part of the command specifies the section and
the variable name followed by the intended value. For example, let's say we are
setting up our *global* git identity on a new machine, and we are setting the
`name` variable, under the `user` tag, to the value `Sadman Kazi`, we issue the
command:
```
git config --global user.name "Sadman Kazi"
```
And with that our global git config file (`~/.gitconfig`) becomes:
```
[user]
    name = Sadman Kazi
```
Other variables can be set the same way.
