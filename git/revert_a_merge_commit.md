# Revert a Merge Commit

Normally running `git merge <commit-hash>` will create a new commit which reverts the previous.

However, merge commits have two parent commits so you also need to tell git which side you wish to keep:

Running `git show <commit-hash>` on the merge commit will list the two parent commits, where:
* The first parent commit was the head of the branch you merged TO
* The second parent commit wass the head of the branch you merged FROM

```
        merge-commit
          /      \
target-branch  destination-branch
```

To specify the parent that you wish to keep (this starts from 1) add `-m <parent-number>`

To revert a merge commit, you're declaring that you want to *keep* the target-branch parent, therefore:
```
git revert -m 1 <merge-commit-hash>
````

## History
Note that this creates a new commit, which reverts the changes from the merge. That means, history is preserved, not overwritten. You can still see that the merge happened.
