Useful aliases: `push --force-with-lease`
===========================================

>Git supports aliases, so we can create custom commands to execute git magic that
>requires too much typing. Aliases can be set by defining them under the `alias`
>section of our git config file.

### git please
```
git config --global alias.please 'push --force-with-lease'
```
Pushing to a remote repository using the force option is dangerous. It basically
rewrites the history by ignoring the upstream branch and replacing it's content
with our local version. This means that any changes that have not been fetched
by the local branch will be erased from history.

This is where the option `--force-with-lease` comes in handy. It checks at least
if the changes/history to be erased has been fetched, doing the force push in a
more **polite** way: `git please`.
