# List All Branches Containing A Commit

"Has this bugfix definitely been merged onto the new branch?"

There's an incredibly quick way of finding this out if you have the commit id to hand: `git branch --contains <commit-hash>`

It will list all branches that contain this commit, and if you're currently checked out on one of those branches. Note that it only looks in local branches, it does not check remotes such as `origin`.


