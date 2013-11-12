Undo My Last n Commits?
$ git reset HEAD~n
This removes the last n commits of a linear history from the
current branch, leaving the corresponding changes in your working
files. You can add --hard to make the working tree reflect the
new branch tip, but beware: this will also discard any current
uncommitted changes, which you will lose with no recourse. 

Reuse the Message from an Existing
Commit?
$ git commit --reset-author -C rev
Add --edit to edit the message before committing.



Reapply an Existing Commit from
Another Branch?
$ git cherry-pick rev
If the commit is in a different local repository, ~/other:
$ git --git-dir ~/other/.git format-patch ↵
-1 --stdout rev | git am

List Files with Conflicts when Merging?
git status shows these as part of its report, but to just list their
names:
$ git diff --name-only --diff-filter=U

Get a Summary of My Branches?
• List local branches: git branch
• List all branches: git branch -a
• Get a compact summary of local branches and status with
respect to their upstream counterparts: git branch -vv
• Get detail about the remote as well: git remote show ori
gin (or other named remote)
