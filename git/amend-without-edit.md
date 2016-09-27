# Edit a Commit without Editing the Message

Sometimes I forget to add something to a git commit, which you can resolve with a simple `git commit --amend`.

However, this brings up an edit dialog. If you don't need to change the edit, this is pointless.
`git commit --amend --no-edit` skips this process and simply amends the existing commit, keeping the message.

It's slightly more characters, so you'll probably want to alias it:
`git config --global alias.amend 'commit --amend --no-edit'`

