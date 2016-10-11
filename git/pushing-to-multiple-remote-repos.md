Pushing to multiple remote repos
================================

Multiple remote URLs can be set to the same remote using the `remote set-url REMOTE_NAME --STREAM --add REMOTE_URL`
command. For example, say we want to assign two different URLs `git@github.com:sadmansk/til.git` (as a `push`
mirror) and `git@git.sadmansk.com:sadmansk/til.git` (original repo) to the same remote `origin`, we can issue
the following commands:

```
$ git remote add origin git@git.sadmansk.com:sadmansk/til.git
$ git remote set-url origin --push --add git@github.com:sadmansk/til.git
$ git remote set-url origin --push --add git@git.sadmansk.com:sadmansk/til.git
```
> Leaving out `--push` will make the remote `pull`-able, which might not be safe.

We can check the current list of URLs attached to all the remotes:
```
$ git remote -v
origin  git@git.sadmansk.com:sadmansk/til.git (fetch)
origin  git@github.com:sadmansk/til.git (push)
origin  git@git.sadmansk.com:sadmansk/til.git (push)
```
