# Bring the Last Commit Back to Staging
*WARNING* Don't do this on any commits that you've pushed to a remote because you're rewriting history

If you've been doing some local development, made a commit, and for some reason would like to bring that back to the stage, you can do so with `git reset --soft HEAD^`.
This is useful if you've committed lots of changes, but want to revist and potentially add them as a series of smaller commits.
