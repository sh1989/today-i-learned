# List Files in Commit

To see what has changed in a commit, you can use `git show <commit-hash>`. But this shows you the contents diff and for large commits, it might be the case that you're only interested in a list of files that have changed.

If this is what you want, use `git show <commit-hash> --name-only`.

Running this on the previous commit to this repo produces:

```
commit 1438db1176efea0fa98b7a19b98cc1d0a8785b9c
Author: Sam Hogarth
Date:   Wed Jun 1 10:10:50 2016 +0100

    TIL about ReactJS functional components

javascript/reactjs/functional_components.md
```
